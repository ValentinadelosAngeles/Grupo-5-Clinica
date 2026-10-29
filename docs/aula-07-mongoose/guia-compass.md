# Roteiro de conferência no MongoDB Compass

A conferência no Atlas e no verificador Nest foi concluída. A conferência visual no Compass permanece pendente: a edição portátil oficial foi obtida e teve hash e assinatura conferidos, mas não abriu janela controlável neste ambiente. Não foi desativada nenhuma proteção do Windows para executá-la.

## Passo a passo para concluir

1. Abra o Compass no PC em que ele esteja funcionando.
2. No Atlas do grupo, use Connect e a opção Compass. Configure a conexão autorizada com o mesmo banco clinora. Use os dados de acesso diretamente no aplicativo; não publique a URI em prints, documentos, issues ou PRs.
3. Abra o banco clinora e a coleção convenios.
4. Em Documents, confira os cinco exemplos. Use o filtro {} para ver todos e { ativo: true } para conferir os quatro ativos.
5. Use { codigoAns: "045678" } para verificar o zero à esquerda. Confira modalidade, createdAt e updatedAt no documento.
6. Em Indexes, confira _id_, convenios_nome_unico, convenios_ans_unico e convenios_ativos_nome.
7. Registre data, responsável e captura sem exibir credenciais. Marque o checklist somente depois da conferência.

## Problemas comuns

- Não conecta: conferir usuário do banco, senha, URI, rede permitida e disponibilidade do cluster com o responsável pelo Atlas. A conta do site Atlas é diferente do usuário do banco.
- Banco ou coleção não aparece: conferir o nome clinora, executar npm run seed com a configuração correta e atualizar a lista de bancos.
- E11000: existe um valor que conflita com um índice único. Não apague o índice para esconder o problema; confira os dados duplicados.
- Dados inválidos entram por edição direta: o schema Mongoose é aplicado pelo model, não automaticamente pelo Compass. O validator da coleção é uma configuração separada.
