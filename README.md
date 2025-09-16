# Sistema de Recomendação baseado em similaridade visual

Este projeto tem como objetivo desenvolver um Sistema de Recomendação baseado em similaridade visual de imagens, utilizando redes de Deep Learning e técnicas de busca em espaço vetorial. 

A proposta é permitir que, a partir da imagem de um produto (ex.: cadeira, bicicleta, caneca), o sistema sugira itens visualmente semelhantes em termos de forma, cor e textura.

O projeto demonstra a viabilidade de um motor de recomendação por imagem, aplicável a e-commerces, catálogos digitais e sistemas de busca visual, proporcionando uma experiência de compra mais intuitiva e personalizada.

- Para a prova de conceito, foi utilizado o **Stanford Online Products Dataset**, um conjunto de mais de 120 mil imagens organizadas por categorias de produtos. 

- A extração de características visuais foi realizada com uma rede **ResNet50 pré-treinada no ImageNet**, onde os embeddings (representações vetoriais das imagens) são gerados a partir da penúltima camada da rede.Esses vetores são então indexados em um mecanismo de busca baseado no **FAISS (Facebook AI Similarity Search)**, que possibilita encontrar rapidamente os produtos mais semelhantes a uma consulta.

O sistema utiliza *transfer learning*, aproveitando uma rede pré-treinada (ResNet50) para extrair embeddings das imagens, evitando treinar do zero.

O fluxo do sistema consiste em:

1. **Pré-processamento** das imagens do dataset.
2. **Extração de embeddings** com CNN pré-treinada.
3. **Indexação dos vetores** em FAISS.
4. **Consulta e recomendação**, retornando produtos similares à imagem fornecida.







