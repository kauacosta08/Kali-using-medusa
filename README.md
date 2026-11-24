# Kali-using-medusa
Exploit de vulnerabilidades no Kali usando Medusa e Metasploitable 2

Como configurei o ambiente:
Seguindo os passos demonstrados ao decorrer das aulas apresentadas, fiz o download e instalação das VM's do Kali Linux (ferramenta principal usada para o pentest) e do Metasploitable 2 (que foi a máquina vulnerável a qual invadimos para fins de teste). Ao iniciar ambas as máquinas solicitamos a instrução "ping -c [IP da máquina vulberável] " dentro do kali linux para ter certeza de que a máquina metasploitable estava acessível.

Ferramentas utilizadas:
A principal ferramenta utilizada para o ataque de força bruta e password spraying foi o Medusa, muito eficiente em cenários que exigem alta velocidade, paralelismo e estabilidade para testar credenciais remotamente em múltiplos serviços ou hosts simultaneamente, podendo rodar em múltiplas threads, como explicado na aula. Porém, possui suas limitações em aplicações web modernas com tokens, ambientes windows, criptografias e etc... Também não podemos descartar o uso do Nmap, que foi uma ferramenta crucial para testar a conectividade entre as duas máquinas e executar uma varredura e scanner de portas abertas e protocolos utilizados pela máquina vulnerável.

Quais foram os testes e como foram executados:
Os principais testes de força bruta aqui executados com o Medusa exigiram a criação de listas de nomes de usuários e possíveis senhas que fariam sentido para a aplicação invadida. Usamos a aplicação web DVWA para a simulação e a frase "Login failed" como parâmetro para que o Medusa entendesse que as credenciais estavam incorretas. Após múltiplas tentativas de combinação, o Medusa encontrava a combinação correta que, ao ser testada no ambiente simulado, concedia o acesso buscado de forma rápida e eficaz. Os ataques utilizados envolveram o brute force (que tentava multiplas combinações de senhas para um determinado usuário) e o password spraying (que tentava poucas senhas em múltiplos usuários).

O que aprendi:
Ao longo das aulas de exploit e pentest aprendi a instalar e configurar um ambiente virtual com Kali Linux e a Metasploitable 2. Além disso aprendi como realizar múltiplos ataques de brute force e password spraying em uma máquina vulnerável, aprendendo também as falhas e as mitigações que estavam faltando na máquina por ser propositalmente vulnerável, como bloqueador por limite de tentativas por IP, bem como Firewall, IDS e IPS... 

Conclusão:
Com a conclusão do desafio posso dizer que foi uma experiência muito interessante e imersiva ao colocar o aluno em contato direto com o ambiente e com as ferramentas utilizadas tanto por atacantes quanto por profissionais da área. Também pude observar o quão necessário é o profissional de segurança tendo em vista a facilidade para que pessoas pouco instruídas na área possam executar ataques bem sucedidos utilizando ferramentas gratuitas, o que se torna um grande desafio para equipes inteiras de defesa conseguirem proteger os seus sistemas.
