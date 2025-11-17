# Documentação Página Informativo & Contato
### Equipe: Cattus

| Integrante | Função no Projeto | Nickname  |
| :--- | :--- | :--- |
| **Vinicius Leal Alves** | Desenvolvedor Fullstack | lealalves |
| **Vinicius Gabriel** | Desenvolvedor Fullstack | gabrigom |
| **Gustavo Kawamoto** | Desenvolvedor Fullstack | kawamotus |

# Descrição da Página **Informativo & Contato**

### Link da Página Hospedada (Deploy): https://gpa-informativo-e-contato.vercel.app/

## Melhorias Visuais (UI/UX)

### Design Visual
- Substituição do template genérico Wix por design customizado moderno
- Nova paleta de cores (roxo/violeta + laranja) com gradientes vibrantes
- Hero section com ilustração SVG e efeito parallax
- Wave dividers decorativas separando seções
- Animações suaves de entrada e hover effects

### Estrutura de Conteúdo
- **Página Informativo**: Conteúdo reorganizado do texto corrido para grid de 8 cards temáticos + warning box destacada para sintomas de hipertermia
- **Página Contato**: Informações divididas em 6 cards visuais com ícones (Endereço, Brechó, Visitação, Email, WhatsApp, Redes Sociais), facilitando escaneabilidade

### Usabilidade
- Layout responsivo e mobile-first
- Navegação clara com header/footer componentizados
- Melhor hierarquia visual e legibilidade (tipografia Jost)
- Código mais leve e performático
- Maior interatividade e feedback visual

## Novas Funcionalidades Implementadas
### Carregamento Dinâmico de Componentes
- Header e footer carregados via JavaScript (fetch)
- Reutilização em múltiplas páginas
- Facilita manutenção centralizada

### Animações com Intersection Observer
- Cards aparecem gradualmente conforme scroll do usuário
- Efeito fade-in + slide-up ao entrar no viewport
- Melhora engajamento e experiência visual

### Efeito Parallax
- Imagem do cachorro no hero se move sutilmente durante o scroll
- Adiciona profundidade e dinamismo à página

### Sistema de Cards Interativos
- Hover effects nos cards de contato e informativo
- Transições suaves entre estados
- Feedback visual imediato ao usuário

### Tratamento de Erros
- Console.error para debug caso componentes não carreguem
