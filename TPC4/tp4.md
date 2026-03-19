**TRABALHO TP4**

Este trabalho prático consistiu no desenvolvimento de um script em python para etxração de informaçção osbre doenças do site em altas da aude, gerando um ficheiro json com a doneça e a respetiva full desc.

reaproveitando a o trabalho realizado em aula , e a execução da função extraoir pagina, desenvolveu-se uma funcao extrair full desc atraves de um link composto pelo url base da pagina + um link este link é correspondetne a cada doença obtido atraves da inspeçao das diferentes div do html disponoivel no site
Este projeto faz scraping do site **Atlas da Saúde** e recolhe, para cada doença listada:
- **Nome** da doença
- **Descrição curta** (resumo da listagem)
- **Descrição completa** (conteúdo da página individual da doença)
Os dados são guardados num ficheiro `doencas.json`, organizado alfabeticamente.

O script irá:
1. Percorrer todas as letras do alfabeto (`/doencas/a`, `/doencas/b`, ...)
2. Extrair todas as doenças listadas em cada página
3. Aceder à página individual de cada doença para obter a descrição completa
4. Guardar tudo no ficheiro `doencas.json`


{
    "Diabetes": {
        "Small_desc": "A diabetes é uma doença crónica...",
        "Full_desc": "A diabetes mellitus é uma perturbação metabólica..."  
},

Assim na small desc devera aparecer a descrição disponivel na pagina de acesso as doenças comecadas por uma certa letra do alfabeto. ja na full_desc deverá retornar toda a descrição disponivel na pagina de acesso de cada doença