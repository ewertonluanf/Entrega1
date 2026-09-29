                Modelagem UML Textual

[Publicação] Classe abstrata

    Atributos privados:
        - _titulo: str
        - _autor: str
        - _ano: int
        - _genero: str
        - _numero_paginas: int
        - _status: str ("NÃO LIDO", "LENDO", "LIDO")
        - _avaliacao: float (0 a 10)
        - _data_inclusao: date
        - _data_inicio: date
        - _data_termino: date
        - _anotacoes: List[Anotacao]

    Métodos:
        - iniciar_leitura(data: date): void
        - concluir_leitura(data: date, avaliacao: float): void
        - adicionar_anotacao(texto: str, trecho: str = None): void
        - __str__(): str
        - __repr__(): str
        - __lt__(other: Publicacao): bool
        - __eq__(other: Publicacao): bool

    Propriedades (@property / setter):
        - titulo
        - autor
        - ano
        - avaliacao
        - status

[Livro]
    - _isbn: str

[Revista]
    - _edicao: int
    - _issn: str

[Anotação]
    Atributos:
        - _data: datetime
        - _texto: str
        - _trecho: str (opcional)
    Métodos:
        - __str__(): str

[Coleção]
    Atributos:
        - _publicacoes: List[Publicacao]

    Métodos:
        - adicionar_publicacao(pub: Publicacao): void
        - remover_publicacao(pub: Publicacao): void
        - buscar_por_titulo(titulo: str): List[Publicacao]
        - buscar_por_autor(autor: str): List[Publicacao]
        - filtrar_por_status(status: str): List[Publicacao]

Relacionamentos:

    - Livro herda de Publicacao.
    - Revista herda de Publicacao.
    - Publicacao possui Anotacoes.
    - Colecao agrupa Publicacoes.
