# Projeto Drupal - Guia para Configuração e Execução

Este projeto foi desenvolvido como parte de um teste prático e segue as melhores práticas para implementação de um site no Drupal. O objetivo é criar um site funcional com recursos específicos detalhados abaixo.

## Requisitos

- **PHP**: Versão 8.1 ou superior.
- **Composer**: Gerenciador de dependências para PHP.
- **DDev**: Para gerenciar o ambiente local de desenvolvimento.
- **Drupal Core**: Versão 11.x.
- **Drush**: Ferramenta de linha de comando para Drupal.

## Instruções para Execução

### 1. Configuração do Ambiente

1. **Instale o Composer**:
   Siga as instruções em [https://getcomposer.org/](https://getcomposer.org/).

2. **Instale o DDev**:
   Configure o DDev conforme detalhado em [https://ddev.readthedocs.io/](https://ddev.readthedocs.io/).

3. **Clone o Repositório**:
   ```bash
   git clone https://github.com/Fe7rodrigues/bootcamp-meu-projeto.git
   cd meu-projeto


*Inicie o Ambiente:*

```
ddev start

```

*Instale as Dependências:*

```
composer install

```

*Inicie o Site:*

```
ddev launch

```

Siga o assistente de instalação do Drupal para configurar o site conforme solicitado.

2. **Configuração de Tipos de Conteúdo e Taxonomias**

**Tipos de Conteúdo:**
**Cachoeiras:**
**Campos:** Nome, Descrição, Altura, Imagem, Localização, Dificuldade.
**Parques de Diversão:**
**Campos:** Nome, Descrição, Fotos, Localização.
**Taxonomias:**
**Vocabulários:** Localização e Dificuldade.

3. **Módulos Instalados**
Os seguintes módulos foram instalados para atender aos requisitos:

*admin_toolbar*
*pathauto*
*token*
*devel*
*gin*

**Instale os módulos com o comando:**

```
composer require drupal/admin_toolbar drupal/pathauto drupal/token drupal/devel drupal/gin

```

4. **Exportação de Configurações e Banco de Dados**

Exportar Configurações:

```
drush config:export

```
*Exportar Banco de Dados*

```
drush sql-dump --result-file=database.sql

```

## Estrutura do Repositório

web/: Contém o código principal do Drupal.
web/modules/contrib/: Módulos instalados via Composer.
web/themes/contrib/: Temas instalados via Composer.
database/: Contém o dump do banco de dados.

## Observações

*Este projeto foi configurado e testado para o Drupal versão 11.x. Certifique-se de seguir as versões especificadas no arquivo composer.json para evitar conflitos de dependências.*


### **O que inclui este `README.md`**
1. **Configuração do ambiente:** Passos para configurar o PHP, Composer e DDev.
2. **Execução do projeto:** Como clonar o repositório, iniciar o ambiente e instalar as dependências.
3. **Configuração de conteúdo e taxonomias:** Detalhes sobre os tipos de conteúdo e taxonomias que devem ser configurados no Drupal.
4. **Instalação de módulos:** Passos para instalar os módulos necessários.
5. **Exportação de configurações e banco de dados:** Como exportar configurações e o banco de dados com Drush.
6. **Estrutura do repositório:** Explicação sobre a organização do repositório.
7. **Observações:** Considerações sobre a versão do Drupal e dependências.

### **Como usar**
1. Copie o conteúdo acima.
2. Crie um arquivo chamado `README.md` na raiz do seu projeto.
3. Cole o conteúdo copiado e salve.

