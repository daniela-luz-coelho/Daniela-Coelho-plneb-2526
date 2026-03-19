**TRABALHO TP4**

Este trabalho prático consistiu no desenvolvimento de um script em Python para extração de informação sobre doenças a partir do site Atlas da Saúde, gerando um ficheiro JSON com o nome da doença e a respetiva descrição completa.

Reaproveitando o trabalho realizado em aula, nomeadamente a função de extração de páginas, foi desenvolvida uma nova função responsável por extrair a descrição completa (full description) de cada doença. Para isso, foi utilizado um link composto pelo URL base do site concatenado com o caminho específico de cada doença, obtido através da inspeção das diferentes div do HTML disponível.


Este trabalho recorre ao site **Atlas da Saúde** e recolhe, para cada doença listada:
- **Nome** da doença
- **Descrição curta** (Small_Desc)
- **Descrição completa** (conteúdo da página individual da doença - Full_Desc)
Os dados são guardados num ficheiro `doencas.json`, organizado alfabeticamente.

O script irá:
1. Percorrer todas as letras do alfabeto (`/doencasaaz/a`, `/doencasaaz/b`, ...)
2. Extrair todas as doenças listadas em cada página
3. Aceder à página individual de cada doença para obter a descrição completa
4. Guardar tudo no ficheiro `doencas.json`

O ficheiro JSON assumirá o seguinte formato:
{
    "Diabetes": {
        "Small_desc": "A diabetes é uma doença crónica...",
        "Full_desc": "A diabetes mellitus é uma perturbação metabólica..."  
},

Assim na Small_Desc do ficheiro JSON deverá constar a descrição ´curta disponvel na página de acesso às doenças iniciadas por uma certa letra do alfabeto. 
Já na full_desc deverá constar toda a descrição disponível na página individual de acesso de cada doença.