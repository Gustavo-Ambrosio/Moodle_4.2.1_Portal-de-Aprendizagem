# Coletivo Darklab - Portal de Aprendizagem

Este projeto consiste na implementação e personalização da plataforma de gestão de aprendizagem (LMS) para o **Coletivo Darklab**, utilizando a plataforma **Moodle**.

A infraestrutura foi projetada para suportar a comunidade Darklab, oferecendo um ambiente robusto para cursos, treinamentos e gestão de conhecimento.

---

## 📂 Estrutura do Projeto

O repositório está organizado de forma a separar o código-fonte da aplicação, os recursos de instalação local e a documentação estratégica:

- **`/Moodle`**: Diretório principal da plataforma.
  - **`public_html/`**: Contém o core do Moodle (versão 4.2.1), responsável pela execução da aplicação web.
  - **`Instalador - Local/`**: Recursos para replicação do ambiente em servidor local.
    - `BKP-comunidade_coletivo_darklab.sql`: Dump do banco de dados MariaDB.
    - `Eu_moodle/`: Pasta com arquivos de dados e configurações específicas.
  - **`Docs/`**: Documentação administrativa, guias de acesso (Ex: Terabox, Feedback Sessions) e padronizações.
- **`/XMind`**: Contém a base estratégica do projeto.
  - `BRIEFING DARKLAB.docx`: Definição de escopo e objetivos.
  - `BUSINESS CASE (DARKLAB).docx`: Estudo de viabilidade e modelo de negócio.
  - `DARKLAB.xmind`: Mapa mental da estrutura organizacional e de conteúdo.

---

## 🚀 Tecnologias Utilizadas

- **Engine**: Moodle 4.2.1 (Build: 20230612)
- **Linguagem**: PHP 8.x
- **Banco de Dados**: MariaDB / MySQL
- **Frontend**: Temas Boost e Classic (Core Moodle)
- **Gerenciadores**: Composer (PHP) e NPM/Grunt (Tasks)

---

## 🛠️ Configuração e Instalação Local

Para rodar o projeto localmente, siga os passos abaixo:

1.  **Requisitos**: Servidor Web (Apache/Nginx), PHP 8.1+, MySQL/MariaDB.
2.  **Arquivos**: Aponte a raiz do seu servidor para a pasta `Moodle/public_html`.
3.  **Banco de Dados**: 
    - Crie um banco de dados vazio.
    - Importe o arquivo `Moodle/Instalador - Local/BKP-comunidade_coletivo_darklab.sql`.
4.  **Configuração de Sistema**:
    - Edite o arquivo `config.php` em `public_html/`.
    - Atualize as credenciais de banco de dados (`$CFG->dbuser`, `$CFG->dbpass`, `$CFG->dbname`).
    - Ajuste o `$CFG->wwwroot` para o seu domínio local (ex: `http://localhost/darklab`).
    - Certifique-se de que o `$CFG->dataroot` aponta para um diretório fora da pasta pública com permissões de escrita.

---

## 📝 Documentação Adicional

Para entender a visão estratégica do Coletivo, consulte os arquivos na pasta [XMind](./XMind). Lá você encontrará o Business Case e o Briefing detalhado que norteiam as decisões deste LMS.

---

## ⚖️ Licença

Este projeto utiliza o Moodle, que é distribuído sob a licença **GNU GPL v3**. Detalhes adicionais podem ser encontrados nos arquivos `COPYING.txt` e `CONTRIBUTING.txt` dentro da pasta `public_html`.

---
*Desenvolvido para o Coletivo Darklab.*
