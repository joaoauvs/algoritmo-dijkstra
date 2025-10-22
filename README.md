# Algoritmo de Dijkstra

Implementação do algoritmo de Dijkstra em C++ para encontrar o caminho mais curto em um grafo ponderado.

## 📋 Descrição

Este projeto implementa o algoritmo de Dijkstra, um algoritmo clássico de teoria dos grafos usado para encontrar o caminho mais curto entre vértices em um grafo com pesos não-negativos nas arestas.

## 🚀 Características

- Implementação eficiente usando fila de prioridade (priority queue)
- Representação do grafo usando lista de adjacências
- Complexidade de tempo: O((V + E) log V), onde V é o número de vértices e E é o número de arestas
- Código comentado e de fácil compreensão

## 📁 Estrutura do Projeto

```
Algoritmo-Dijkstra/
├── Dijkstra.cpp      # Implementação do algoritmo
└── README.md         # Documentação do projeto
```

## 🛠️ Como Compilar

Para compilar o programa, use o g++ (ou qualquer compilador C++):

```bash
g++ -o dijkstra Dijkstra.cpp -std=c++11
```

## ▶️ Como Executar

Após a compilação, execute o programa:

```bash
./dijkstra
```

## 📊 Exemplo de Uso

O código atual cria um grafo com 5 vértices (0 a 4) e as seguintes arestas ponderadas:

```
Vértice 0 → Vértice 1 (peso: 4)
Vértice 0 → Vértice 2 (peso: 2)
Vértice 0 → Vértice 3 (peso: 5)
Vértice 1 → Vértice 4 (peso: 1)
Vértice 2 → Vértice 1 (peso: 1)
Vértice 2 → Vértice 3 (peso: 2)
Vértice 2 → Vértice 4 (peso: 1)
Vértice 3 → Vértice 4 (peso: 1)
```

O programa calcula e exibe o menor caminho do vértice 0 ao vértice 4.

**Resultado esperado:** 3

**Caminho:** 0 → 2 → 4 (custo total: 2 + 1 = 3)

## 🔧 Como Modificar

Para usar o algoritmo com seu próprio grafo, modifique a função `main()`:

```cpp
int main() {
    // Crie um grafo com N vértices
    Grafo g(N);

    // Adicione arestas: g.addAresta(origem, destino, peso)
    g.addAresta(0, 1, 10);
    g.addAresta(1, 2, 5);
    // ... adicione mais arestas

    // Calcule a distância mínima
    int origem = 0;
    int destino = 2;
    cout << "Distância mínima: " << g.dijkstra(origem, destino) << endl;

    return 0;
}
```

## 🧮 Como Funciona

1. **Inicialização:** Todas as distâncias são definidas como infinito, exceto a origem (0)
2. **Fila de Prioridade:** Os vértices são processados em ordem de menor distância
3. **Relaxamento:** Para cada vértice, atualiza as distâncias dos vizinhos se um caminho mais curto for encontrado
4. **Resultado:** Retorna a menor distância até o vértice de destino

## 📚 Conceitos Utilizados

- **Grafo Ponderado:** Grafo onde cada aresta tem um peso (custo) associado
- **Lista de Adjacências:** Estrutura de dados eficiente para representar grafos esparsos
- **Fila de Prioridade:** Estrutura que mantém elementos ordenados por prioridade (menor distância primeiro)
- **Algoritmo Guloso:** Sempre escolhe o vértice com menor distância não visitado

## ⚙️ Requisitos

- Compilador C++ com suporte a C++11 ou superior
- Sistema operacional: Windows, Linux ou macOS

## 📝 Notas

- O algoritmo assume que os pesos das arestas são não-negativos
- Para grafos com pesos negativos, considere usar o algoritmo de Bellman-Ford
- A constante `INFINITO` é definida como 10000000 (pode ser ajustada conforme necessário)

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para:
- Reportar bugs
- Sugerir melhorias
- Enviar pull requests

## 📄 Licença

Este projeto é de código aberto e está disponível para fins educacionais.

---

**Autor:** João Augusto
**Última atualização:** Outubro 2024
