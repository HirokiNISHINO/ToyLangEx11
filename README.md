# ToyLangEx11
Toy Programming Language: Ex11

グローバル変数への代入をサポート

現状の文法．

\<Program\> ::= \<Statements\>

\<Statements\> ::= [\<Statement\>]\*

\<Statement\> :: = \<ExprStmt>　| \<EmptyStmt\> | \<Global\>

\<Global\> ::= 'global' \<Type\> Identifier ';'

\<Type\> ::= 'int'

\<ExprStmt> ::= \<AdditiExpr\>　 ';'

\<EmptyStmt\> :: = ';'

\<AdditiExpr\>　:: = \<MultiplicativeExpr\> [ ( '+' | '-' ) \<MultiplicativeExpr\> ]\*

\<MultiplicativeExpr\> :: = \<Primary\> [ ( '\*'  | '/' ) \<Primary\> ]\*

\<Primary\> :: = ( \<AdditiExpr\> ) | \<Integer\>　| \<IdentifierOrAssignment\>　

\<IdentifierOrAssignment\>　 ::= \<Identifier\>　( '=' \<AdditiExpr\>)
