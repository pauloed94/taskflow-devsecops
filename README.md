1. O que você entendeu pela expressão "shift-left security"?

Shift-left security significa pensar em segurança desde o início do desenvolvimento, e não apenas quando o sistema já está pronto. A ideia é identificar vulnerabilidades o mais cedo possível, durante o planejamento, desenvolvimento e testes. Dessa forma, os problemas podem ser corrigidos antes de chegarem à produção, evitando retrabalho e reduzindo os riscos.

2. Cite pelo menos uma vulnerabilidade observada no TaskFlow e explique por que ela pode ser um problema.

Um problema observado no TaskFlow foi o uso de credenciais muito simples, como `admin/admin123`. Uma senha desse tipo é fácil de descobrir ou tentar em um ataque de força bruta. Caso isso aconteça em uma aplicação real, um invasor poderia conseguir acesso a uma conta administrativa e obter permissões que não deveria possuir.

3. Por que esperar até o fim do desenvolvimento para pensar em segurança é arriscado?

Porque uma vulnerabilidade descoberta no final pode exigir mudanças em partes que já estavam consideradas prontas. Isso aumenta o retrabalho, o custo e o tempo necessário para corrigir o problema. Além disso, existe o risco de alguma falha não ser encontrada antes da aplicação entrar em produção. Por isso, faz mais sentido realizar verificações de segurança durante todo o desenvolvimento.
