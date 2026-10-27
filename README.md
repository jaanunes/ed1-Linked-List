ED1 - Lista Encadeada em C++
Projeto desenvolvido em C++ para estudar e implementar uma lista simplesmente encadeada genérica, utilizando templates, alocação dinâmica de memória e operações comuns de estruturas de dados.
📚 Sobre o projeto
A implementação define uma interface abstrata List<T> e uma classe LinkedList<T> que implementa essa interface. Cada nó armazena um elemento e um ponteiro para o próximo nó.

A lista mantém ponteiros para o primeiro (head) e o último (tail) nó, além de um contador de elementos (count).
✨ Funcionalidades
- Inserir elemento no início: addFirst()
- Inserir elemento no final: addLast()
- Inserir em uma posição específica: insertAt()
- Inserir mantendo a ordem crescente: addSorted()
- Remover o primeiro elemento: removeFirst()
- Remover o último elemento: removeLast()
- Remover por índice: removeAt()
- Remover a primeira ocorrência de um valor: remove()
- Buscar um elemento e retornar seu índice: find()
- Obter elemento por índice: get()
- Atualizar elemento por índice: set()
- Consultar quantidade de elementos: size()
- Verificar se a lista está vazia: isEmpty()
- Limpar todos os elementos: clear()
- Exibir a lista em formato de texto: toString()
A classe é genérica (LinkedList<T>), portanto pode armazenar diferentes tipos de dados, desde que o tipo utilizado ofereça as operações necessárias para cada método.
🗂️ Estrutura de arquivos
ed1-Linked-List/
├── include/
│   ├── List.h              # Interface abstrata da lista
│   └── LinkedList.h        # Implementação da lista encadeada
├── src/
│   └── LinkedListTest.cpp  # Testes e exemplos de uso
├── main.cpp                # Programa principal inicial
├── CMakeLists.txt          # Configuração de compilação com CMake
└── README.md               # Documentação do projeto
🛠️ Tecnologias e conceitos
- C++
- C++20
- Templates
- Classes abstratas e métodos virtuais
- Ponteiros e alocação dinâmica (new / delete)
- Lista simplesmente encadeada
- Tratamento de exceções
- CMake
🚀 Como compilar e executar
É necessário ter um compilador C++ compatível com C++20 e o CMake instalados.
Usando CLion
1. Abra a pasta do projeto no CLion.
2. Aguarde o carregamento e a configuração do CMake.
3. Selecione o alvo ed1_linked_list_cpp para executar o main.cpp.
4. Para executar os testes, selecione o alvo LinkedListTest.
Usando o terminal
Na pasta raiz do projeto, execute:
cmake -S . -B build
cmake --build build
Depois, execute o programa principal:
./build/ed1_linked_list_cpp
Para executar os testes:
./build/LinkedListTest
No Windows, o caminho do executável pode variar conforme o gerador utilizado pelo CMake. Em geradores como Visual Studio, os executáveis podem ficar dentro de uma subpasta de configuração, como Debug.
🧪 Testes incluídos
O arquivo src/LinkedListTest.cpp contém exemplos de teste para:
- Inserção no início e no final;
- Inserção por posição;
- Remoção no início, no final, por índice e por valor;
- Busca e acesso por índice;
- Atualização de elementos;
- Inserção ordenada;
- Uso da lista nativa std::forward_list para comparação ilustrativa.
Os testes exibem os resultados esperados e os resultados obtidos no terminal. Eles são exemplos executáveis, não um framework formal de testes unitários.
⚠️ Observações
- Os índices começam em 0.
- find() retorna -1 quando o elemento não é encontrado.
- get(), set() e operações por índice inválido lançam std::invalid_argument.
- removeFirst() e removeLast() lançam std::runtime_error quando a lista está vazia.
- addSorted() insere em ordem crescente e depende do operador < para o tipo armazenado.
- O main.cpp atual é apenas um exemplo inicial; as operações da lista são demonstradas principalmente em src/LinkedListTest.cpp.
🎓 Objetivo acadêmico
O projeto serve como material de estudo para a disciplina de Estrutura de Dados, permitindo compreender como uma lista encadeada funciona internamente e como implementar operações de inserção, remoção, busca e acesso sem utilizar um vetor como estrutura principal.
Projeto: ED1 - Linked List
Linguagem: C++20
