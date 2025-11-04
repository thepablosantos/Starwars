# 🌟 Star Wars Characters - Projeto de Treinamento JavaScript

![Star Wars Characters](https://img.shields.io/badge/Star%20Wars-Characters-yellow?style=for-the-badge&logo=star-wars)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

## 📋 Sobre o Projeto

Este projeto é uma aplicação web interativa desenvolvida para explorar e exibir informações sobre os personagens do universo Star Wars. Foi criado como um projeto de treinamento para praticar JavaScript moderno, consumo de APIs, manipulação do DOM, e criação de interfaces responsivas.

A aplicação consome dados da [SWAPI (Star Wars API)](https://swapi.dev/) e da [Star Wars API](https://akabab.github.io/starwars-api/) para exibir personagens com suas informações detalhadas em cards interativos.

## 🖼️ Preview do Projeto

![Star Wars Characters Website](./assets/screen.png)

*Interface do projeto mostrando os cards de personagens de Star Wars*

## ✨ Funcionalidades

### 🎯 Principais Recursos

- **📊 Listagem de Personagens**: Exibe todos os personagens de Star Wars em formato de cards
- **🖼️ Imagens Dinâmicas**: Cada personagem possui sua imagem correspondente carregada dinamicamente
- **📱 Modal Informativo**: Ao clicar em um card, abre um modal com informações detalhadas do personagem:
  - Altura
  - Peso
  - Cor do cabelo
  - Cor da pele
  - Cor dos olhos
  - Ano de nascimento
  - Gênero
- **⬅️➡️ Paginação**: Sistema de navegação entre páginas com botões "Voltar" e "Avançar"
- **🎨 Design Temático**: Interface inspirada no universo Star Wars com animações suaves
- **📱 Responsivo**: Layout adaptável para diferentes tamanhos de tela

## 🛠️ Tecnologias Utilizadas

### Frontend
- **HTML5**: Estrutura semântica da aplicação
- **CSS3**: 
  - Flexbox e Grid para layout
  - Animações e transições
  - Gradientes e efeitos visuais
  - Fontes temáticas (Star Wars Font)
- **JavaScript (ES6+)**:
  - Async/Await para requisições assíncronas
  - Fetch API para consumo de APIs
  - Manipulação do DOM
  - Event Listeners
  - Template Literals

### APIs e Bibliotecas
- **SWAPI (Star Wars API)**: https://swapi.dev/
  - Endpoint: `/api/people/`
  - Retorna dados dos personagens
  
- **Star Wars API (akabab)**: https://akabab.github.io/starwars-api/
  - Endpoint: `/api/id/{id}.json`
  - Fornece imagens dos personagens

- **Font Awesome**: Ícones para redes sociais
- **Google Fonts**: Fonte Star Wars para tipografia temática

## 📁 Estrutura do Projeto

```
Starwars/
│
├── assets/                 # Arquivos de mídia e imagens
│   ├── starwars1.jpg      # Background principal
│   ├── starwars2.jpg      # Background alternativo
│   ├── luke.jpg           # Imagem padrão de fallback
│   ├── starlogo*.png      # Logos do Star Wars
│   └── millenium-falcon.png
│
├── index.html             # Estrutura HTML principal
├── style.css              # Estilos e animações
├── script.js              # Lógica JavaScript
└── README.md              # Documentação do projeto
```

## 🚀 Como Executar

### Pré-requisitos
- Navegador moderno (Chrome, Firefox, Edge, Safari)
- Servidor web local (opcional, pode abrir direto no navegador)

### Instalação e Execução

1. **Clone o repositório**:
```bash
git clone https://github.com/seu-usuario/starwars-characters.git
cd starwars-characters
```

2. **Abra o projeto**:
   - Opção 1: Abra o arquivo `index.html` diretamente no navegador
   - Opção 2: Use um servidor local (recomendado):
   
```bash
# Com Python 3
python -m http.server 8000

# Com Node.js (http-server)
npx http-server

# Com PHP
php -S localhost:8000
```

3. **Acesse no navegador**:
   - Se usar servidor local: `http://localhost:8000`
   - Se abrir direto: Navegue até o arquivo `index.html`

## 📚 Conceitos de JavaScript Praticados

Este projeto foi desenvolvido para treinar e demonstrar os seguintes conceitos:

### 🔹 Async/Await e Promises
```javascript
async function loadCharacters(url) {
    const response = await fetch(url);
    const responseJson = await response.json();
    // ...
}
```

### 🔹 Fetch API
- Consumo de APIs RESTful
- Tratamento de erros
- Manipulação de respostas JSON

### 🔹 Manipulação do DOM
- Criação dinâmica de elementos
- Inserção de conteúdo
- Adição de event listeners

### 🔹 Template Literals
```javascript
card.style.backgroundImage = `url('${imageUrl}')`;
```

### 🔹 Arrow Functions
```javascript
card.addEventListener('click', () => openCharacterModal(character));
```

### 🔹 Destructuring
- Extração de dados de objetos JSON
- Desestruturação de arrays

### 🔹 Map e Estruturas de Dados
- Mapeamento de nomes para IDs
- Manipulação de arrays com métodos modernos

### 🔹 Gerenciamento de Estado
- Controle de URLs de paginação
- Estado dos botões de navegação

## 🎨 Características do Design

- **Paleta de Cores**: Tons escuros (preto, azul escuro) com acentos dourados
- **Tipografia**: Fonte Star Wars para elementos temáticos
- **Animações**: Transições suaves em hover e interações
- **Layout**: Cards responsivos com efeitos visuais
- **Background**: Imagem temática de Star Wars com overlay escuro

## 🔧 Funcionalidades Técnicas Detalhadas

### Sistema de Paginação
- Detecta automaticamente se há páginas anteriores/próximas
- Habilita/desabilita botões conforme disponibilidade
- Evita duplicação de event listeners

### Carregamento de Imagens
- Sistema de mapeamento de personagens para IDs
- Fallback para imagem padrão caso a imagem não seja encontrada
- Carregamento assíncrono de imagens

### Modal Interativo
- Fecha ao clicar fora ou no botão X
- Animações de entrada e saída
- Exibição formatada de informações

## 📝 Melhorias Futuras

- [ ] Adicionar filtro de busca por nome
- [ ] Implementar favoritos de personagens
- [ ] Adicionar mais informações (planetas, naves, filmes)
- [ ] Sistema de cache para melhor performance
- [ ] Loading skeleton durante carregamento
- [ ] Modo escuro/claro (toggle)
- [ ] Testes unitários

## 👨‍💻 Autor

**Pablo Sodré**

- GitHub: [@thepablosantos](https://www.github.com/thepablosantos)
- LinkedIn: [pablo-sodre](https://www.linkedin.com/in/pablo-sodre)
- Portfolio: [Pablo Sodré](https://www.pablosantos.xyz/ )

## 📄 Licença

Este projeto foi criado apenas para fins educacionais e de treinamento.

## 🙏 Agradecimentos

- [SWAPI](https://swapi.dev/) - Pela API gratuita de Star Wars
- [Star Wars API (akabab)](https://akabab.github.io/starwars-api/) - Pelas imagens dos personagens
- [Font Awesome](https://fontawesome.com/) - Pelos ícones
- [Star Wars Fonts](https://www.cdnfonts.com/star-wars.font) - Pela tipografia temática

## 📖 Recursos de Aprendizado

Este projeto demonstra:

- ✅ Consumo de APIs REST
- ✅ JavaScript assíncrono
- ✅ Manipulação de DOM
- ✅ Event handling
- ✅ CSS moderno (Flexbox, Animations)
- ✅ Responsive design
- ✅ Estruturação de código JavaScript
- ✅ Tratamento de erros
- ✅ UX/UI design

---

⭐ **Desenvolvido com 💛 e a Força** ⭐

*"Que a Força esteja com você!"*
