# case-dp6
Onboarding case w/ JS, collecting events w/ GTM.

# Eventos a serem configurados #


# Dimensão Personalizada 1: #

**User DP6:** Deve ser enviado em todos os eventos de Visualização de Página e Interações a Dimensão Personalizada 1 (Custom Dimension 1 ou CD1) com o seu DP6 User (usuário DP6). O DP6 User é a primeira parte do seu e-mail antes do @ usando a criptografia MD5, por exemplo:

**51a7ff44ccf512e78ddb905270830774**  
**e4c06fd1a1f9dbeae0ad586a681fe675**  

# Dimensão Personalizada 2: #

**GTM ID:** Deve ser enviado em todos os eventos de Visualização de Página e Interações a Dimensão Personalizada 2 (Custom Dimension 2 ou CD2) com o ID do seu GTM, por exemplo:

**GTM-87F13K**  
**GTM-66AQ12**  

# Dimensão Personalizada 3: #

**GTM Version:** Deve ser enviado em todos os eventos de Visualização de Página e Interações a Dimensão Personalizada 3 (Custom Dimension 3 ou CD3) com a versão do container do seu GTM, por exemplo:

**1**  
**2**  
**3**  

Precisamos que, **em todas as páginas**, seja enviado uma **Visualização de Página**. Ela não deverá possuir configuração nenhuma, apenas enviando uma visualização padrão de acordo com a documentação.

Além disso, gostaríamos que fossem implementados alguns eventos de interação na interação de alguns elementos. Implemente Eventos de acordo com o padrão solicitado em cada página, utilizando o modelo de AddEventListener ou OnClick:

# Todas as páginas #

No menu, há um link que direciona o usuário para a página de contato da DP6. Configure um evento como o seguinte:

**Categoria:** “menu”  
**Ação:** “entre_em_contato”  
**Rótulo:** “link_externo”  

Também há um link que inicializa o download de um conteúdo. Configure um evento como o seguinte:


**Categoria:** “menu”  
**Ação:** “download_pdf”  
**Rótulo:** “download_pdf”  

# Página analise.html #

Sempre que um dos botões **lorem, ipsum e dolor** for clicado, configure o envio do seguinte evento customizado:

**Categoria:** “analise”  
**Ação:** “ver_mais”  
**Rótulo:** [nome_do_conteudo]*  


**Substitua [nome_do_conteudo] pelo nome do botão, como “Lorem”, “Ipsum” e “Dolor”.**

# Página sobre.html #

Implemente os seguintes eventos ao preencher **cada um dos campos do formulário:**

**Categoria:** “contato”  
**Ação:** [nome_do_campo]*  
**Rótulo:** “preencheu”  


**Substitua [nome_do_campo] pelo nome do campo preenchido, dentre “nome”, “email”, “telefone” ou “aceito”.**

Quando o formulário for enviado, será exibido um popup. **Na exibição deste popup**, envie o seguinte evento:

**Categoria:** “contato”  
**Ação:** “enviado”  
**Rótulo:** “enviado”  
