# Banco-de-Dados-Biblioteca
Modelagem de Banco de Dados - DSM - Avaliação Final - 1º Semestre


CENÁRIO


-Esta biblioteca valoriza muito a leitura através de livros físicos, pois acredita assim os leitores conseguem se conectar mais profundamente com a história. Assim, como uma forma de manter as tradições e apoiar seu ponto de vista, todos os registros são feitos no papel. Entretanto, com o crescimento da biblioteca e o aumento no número de clientes, começaram a surgir alguns problemas. Ficou complicado encontrar a localização de todos os livros, saber quais estavam em bom estado e quais precisavam ser trocados, quantos exemplares havia de cada um, quais foram emprestados e qual já foram devolvidos, etc. Dessa forma, os proprietários decidiram se modernizar um pouco e investir em um banco de dados.


ENTIDADES E ATRIBUTOS


AS - Atributo Simples

AC - Atributo Composto

AM - Atributo Multivalorado

AD - Atributo Derivado

AI - Atributo Identificador

Livro --> id_livro(AI), titulo_livro(AS), nome_autor(AS), ano_publicacao(AS), genero_livro(AM).

Editora --> Id_editora(AI), nome_editora(AS), endereco(AC), logradouro(AS), cep(AS), numero(AS), bairro(AS), cidade(AS), estado(AS).

Leitor --> id_leitor(AI), nome_leitor(AS), email_leitor(AM), telefone(AS), idade(AD), data_nascimento(AS.

Carteira_da_Biblioteca --> id_carteira(AI), id_leitor(AI), validade(AS), status(AS).

Exemplar --> id_exemplar(AI), estado_de_conservacao(AS), codigo_de_barras(AS).

Localizacao --> id_localizacao(AI), andar(AS), setor(AS), corredor(AS), estante(AS), prateleira(AS).

Emprestimo --> id_emprestimo(AI), id_exemplar(AI), id_carteira(AI), data_emprestimo(AS), data_devolucao(AS).


RELACIONAMENTOS


Leitor (1:1) Carteira_da_Biblioteca

Livro (N:N) Leitor

Livro (N:1) Editora

Livro (1:N) Exemplar

Exemplar (N:1) Localizacao

Exemplar (1:N) Emprestimo
