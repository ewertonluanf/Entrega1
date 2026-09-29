# Biblioteca Pessoal Digital

Um sistema para gerenciar uma biblioteca pessoal de livros e revistas digitais, permitindo o cadastro e o registro das leituras status e relatórios da coleção.

# Objetivo
O projeto visa aplicar conceitos de Programação Orientada a Objetos (POO) em Python:
- Encapsulamento e validações com `@property`.
- Herança simplis e multipla.
- Métodos especiais(`__str__`,`__repr`,`__lt__`,`__eq__`).
- Padrões de projeto (Strategy / State / Repository).
- Persistência em JSON/SQLite.
- Testes automatizados com `pytest`.

# Estrutura Planejada de Classes

1. `Publicação`: Classe abstrata base com atributos comuns da coleção.
2. `Livro`: Especialização de publicação contendo ISBN.
3. `Revista`: Especialização de publicação contendo edição e ISSN.
4. `Anotação`: Representa notas e trechos vinculados as publicações.
5. `Coleção`: Agrupa e gerencia a lista de publicações.
6. `RelatorioService`: Serviço para cálculo de metricas e estatísticas.
7. `DadosRepository`: Camada de armazenamento de dados.
