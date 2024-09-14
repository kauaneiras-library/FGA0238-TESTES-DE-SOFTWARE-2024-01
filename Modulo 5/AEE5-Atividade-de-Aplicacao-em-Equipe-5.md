# Atividades de Aplicação em Equipe 5 (AAE-5): Teste de Segurança - Análise SAST

## Enunciado

### Objetivo:
Realizar análise estática de código utilizando o **SonarQube Community Edition** ou **SonarCloud** para identificar vulnerabilidades de segurança e security hotspots.

### Instruções:

1. Instalar o SonarQube Community Edition ou abrir o SonarCloud:
   - https://www.sonarsource.com/products/sonarqube/downloads/
   - https://sonarcloud.io/

2. Realizar a análise estática do código da aplicação open-source que a equipe está utilizando.
3. Identificar as vulnerabilidades e security hotspots.
4. Selecionar uma vulnerabilidade para análise:
   - Dar preferência para vulnerabilidades na lista da **OWASP Top 10** (https://owasp.org/www-project-top-ten/).
   
5. Analisar a vulnerabilidade selecionada:
   - Descrever com suas palavras o problema identificado pela ferramenta.
   - Verificar se se trata de um problema real ou falso positivo. Justificar a resposta.
   - Sugerir uma solução para resolver o problema.
   
### Entrega:
- O relatório deve conter:
   - Visão geral do resultado da análise estática completa do software (Bugs, vulnerabilidades, security hotspots, dívida técnica, linhas de código, etc.).
   - Captura das telas do resultado da análise.
   - Identificação, descrição, análise e solução para a vulnerabilidade selecionada.

---

## Resolução

### 1. Aplicação Analisada

#### 1.1. Identificação da Aplicação
- **Nome**: MEC-Energia
- **Link para o repositório**: [MEC-Energia GitLab](https://gitlab.com/lappis-unb/projetos-energia/mec-energia)

#### 1.2. Descrição
- O projeto **MEC-Energia** é um sistema de recomendação de contratos de energia elétrica, desenvolvido para auxiliar as Instituições de Ensino Superior (IES) a gerenciar e avaliar a adequação dos seus contratos de energia.
- O sistema permite o registro de faturas mensais de energia e gera relatórios que sugerem ajustes nos contratos, otimizando o consumo e economizando recursos.

#### 1.3. Linguagens Utilizadas
- **Frontend**: Typescript
- **Backend**: Python

---

### 2. Visão Geral do Resultado

A análise foi realizada no backend da aplicação **MEC-Energia API**. A seguir está a captura de tela do resultado da análise estática utilizando o SonarCloud:

![SonarCloud Resultados](caminho_da_imagem.png)

- **Security Hotspots**: 27 detectados.
- **Bugs**: 13 identificados.
- **Code Smells**: 181 detectados.
- **Cobertura de Testes**: O SonarCloud relatou uma cobertura de testes de 0,0%, embora a cobertura real do projeto seja de 59%.

---

### 3. Vulnerabilidades

Nenhuma vulnerabilidade foi identificada pela ferramenta, o que sugere uma boa conformidade com as práticas de segurança, mas exige monitoramento contínuo.

---

### 4. Security Hotspots

A seguir está a lista dos **security hotspots** identificados:

1. **Authentication (20)**:
   - "password" detected here, review this potentially hard-coded credential. (20 ocorrências)
   
2. **Cross-Site Request Forgery (CRSF) (1)**:
   - Make sure allowing safe and unsafe HTTP methods is safe here.
   
3. **Permission (2)**:
   - Copying recursively might inadvertently add sensitive data to the container.
   - The python image runs with root as the default user. Make sure it is safe here.
   
4. **Weak Cryptography (1)**:
   - Make sure that using this pseudorandom number generator is safe here.
   
5. **Encryption of Sensitive Data (1)**:
   - Using HTTP protocol is insecure. Use HTTPS instead.
   
6. **Insecure Configuration (1)**:
   - Make sure this permissive CORS policy is safe here.
   
7. **Outros (1)**:
   - Make sure automatically installing recommended packages is safe here.

---

### 5. Análise de Vulnerabilidades ou Hotspots

#### 5.1. Vulnerabilidade Selecionada: **Authentication**

##### 5.1.1. Descrição
- **"password" detected here, review this potentially hard-coded credential.**
- O hotspot sugere que credenciais hard-coded foram detectadas, o que é uma prática insegura. Senhas diretamente no código podem ser extraídas facilmente, levando a comprometimento de segurança.

##### 5.1.2. Análise de Falso Positivo:
- Após a análise, verificou-se que a instância detectada não é uma credencial armazenada de forma insegura, mas sim um uso legítimo de credenciais em scripts que criam dados iniciais (seed data) para um ambiente de desenvolvimento ou teste.
- Como essas credenciais não são usadas em produção, este pode ser considerado um **falso positivo**.
- Entretanto, boas práticas recomendam evitar o hard-coding de senhas mesmo em ambientes de desenvolvimento, sugerindo o uso de métodos alternativos para carregar essas informações.

##### 5.1.3. Solução:
- Verificar se as credenciais são usadas apenas para testes e não em produção.
- Separar as credenciais de seed data do código-fonte principal.
- Usar variáveis de ambiente para carregar credenciais de forma segura, mesmo em ambientes de desenvolvimento.
- Documentar o uso dessas credenciais para evitar mal-entendidos no futuro.

---

### 6. Conclusão

A análise do projeto **MEC-Energia API** não detectou vulnerabilidades significativas, porém identificou 27 security hotspots que exigem revisão manual. Após a análise de um dos principais hotspots, foi determinado que se tratava de um **falso positivo**, mas medidas de segurança foram sugeridas para aprimorar o código.
