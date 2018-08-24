# Ciandt Angular Challenge

Criar um projeto Angular que liste os pokemons e exiba os seus detalhes quando clicar em um deles.

---
Deverão ser criados os componentes

- Home : Onde ficará o título de boas vindas ao app (Path : "")
- PokemonList : Onde serão listados os pokemons (Path : "PokemonList")
- PokemonDetail : Onde serão exibidos os detalhes do pokemon selecionado (Path : "PokemonDetail/:id")
---
Deverá ser criado um serviço que:

- Recupera todos os pokemons
- Recupera um pokemon baseado no id
---
A API de acesso é a seguinte (não é necessário nenhum token de autenticação)

https://pokeapi.co/api/v2/pokemon/?limit=10&offset=0   
Recupera os pokemons com um limite de 10 e um offset de 0

O objeto de retorno
```sh
{
"count": 949, // Contagem total de Pokemons
"previous": null, // Endereço da lista anterior, caso haja
"results": [
    {
        "url": "https://pokeapi.co/api/v2/pokemon/1/",
        "name": "bulbasaur"
    }
], // Array de objetos com os resultados (Nesse caso eu omiti o restante para essa documentação)
"next": "https://pokeapi.co/api/v2/pokemon/?limit=10&offset=10" // Endereço da próxima lista
}
```

# Momento Gambiarra

Para selecionar um pokemon é necessário accessar essa url:
- https://pokeapi.co/api/v2/pokemon/1/

Onde o "1" é o id do pokemon, dependendo da forma que você construir o serviço, será necessário passar ou essa url inteira ou pegar apenas o id "1" e passar para o serviço. Não é culpa minha, culpa da api que não fornece um campo isolado com o ID.
