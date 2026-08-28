1. O que você entendeu pela expressão "shift-left security"?

Shift-left security significa pensar em segurança desde o início do desenvolvimento, e não apenas quando o sistema já está pronto. A ideia é identificar vulnerabilidades o mais cedo possível, durante o planejamento, desenvolvimento e testes. Dessa forma, os problemas podem ser corrigidos antes de chegarem à produção, evitando retrabalho e reduzindo os riscos.

2. Cite pelo menos uma vulnerabilidade observada no TaskFlow e explique por que ela pode ser um problema.

Um problema observado no TaskFlow foi o uso de credenciais muito simples, como `admin/admin123`. Uma senha desse tipo é fácil de descobrir ou tentar em um ataque de força bruta. Caso isso aconteça em uma aplicação real, um invasor poderia conseguir acesso a uma conta administrativa e obter permissões que não deveria possuir.

3. Por que esperar até o fim do desenvolvimento para pensar em segurança é arriscado?

<<<<<<< HEAD
Porque uma vulnerabilidade descoberta no final pode exigir mudanças em partes que já estavam consideradas prontas. Isso aumenta o retrabalho, o custo e o tempo necessário para corrigir o problema. Além disso, existe o risco de alguma falha não ser encontrada antes da aplicação entrar em produção. Por isso, faz mais sentido realizar verificações de segurança durante todo o desenvolvimento.
"# Teste de Pull Request para validar o CI" 
=======
- Use este código como referência de boas práticas.
- Implante esta aplicação em ambiente de produção ou exposto à internet.
- Reutilize o padrão de código (concatenação de SQL, senhas em texto puro,
  segredo hardcoded) em projetos reais.

## Como executar localmente

```bash
cd app-exemplo
python3 -m venv .venv
source venv/bin/activate          # Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

A aplicação sobe em `http://localhost:5000`. Usuários de teste já vêm
cadastrados no banco SQLite (`taskflow.db`, criado automaticamente):

| Usuário | Senha    |
|---------|----------|
| admin   | admin123 |
| aluno   | senha123 |

## Como executar com Docker

```bash
cd app-exemplo
docker build -t taskflow:vuln .
docker run -p 5000:5000 taskflow:vuln
```

## Estrutura

```
app-exemplo/
├── app.py              # Aplicação Flask (versão vulnerável, linha de base)
├── requirements.txt    # Dependências com CVEs conhecidas (uso proposital)
├── Dockerfile           # Dockerfile inseguro (uso no Módulo 2 - Hardening)
└── README.md            # Este arquivo
```

Cada módulo cria, dentro da sua própria pasta `codigo/`, uma cópia ou um
patch desta aplicação demonstrando o "antes" (vulnerável) e o "depois"
(corrigido) referente ao tema daquele encontro.

## Teste de proteção do branch

Mudança de teste.

Teste 3 - A hora de morrer
>>>>>>> df2ce718c6cb12012502414f0cff7dcd29349014
