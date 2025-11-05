# AppLocaliza2

Aplicativo móvel construído com Expo + React Native que permite obter a localização do usuário, buscar endereços, salvar locais no banco de dados :contentReference[oaicite:0]{index=0} e visualizar mapas usando duas APIs distintas (:contentReference[oaicite:1]{index=1} e :contentReference[oaicite:2]{index=2}).

---

## 🧪 Funcionalidades

- Obter a localização atual do usuário via GPS.  
- Buscar um endereço e converter em coordenadas (geocodificação).  
- Exibir o mapa com marcador no local buscado.  
- Salvar locais no Supabase (nome, latitude, longitude, timestamp).  
- Listar os locais salvos e exibir no painel.  
- Duas implementações de mapa para comparação: Google Maps vs Mapbox.  
- Deletar locais (na versão Mapbox, se implementado).

---

## 🧰 Tecnologias

- Expo SDK 54  
- React Native  
- Supabase (backend e banco de dados)  
- Axios (requisições HTTP)  
- WebView (para exibir os mapas JavaScript)  
- Expo-Location (pegar localização do dispositivo)  
- React Navigation (navegação por abas)  

---

## 🚀 Instalação e execução

1. Clone o repositório:  
   ```bash
   git clone https://github.com/<seu-usuario>/<nome-repositorio>.git
   cd <nome-repositorio>

2. Instale dependências:
   npm install

3. Execute o projeto:
   npm start
   Escolha abrir no Android, iOS ou Web.

 ## 🗂️ Estrutura de pastas
 /services
  ├─ locationService.js
  ├─ supabaseClient.js
/screens
  ├─ GoogleMapsScreen.js
  ├─ MapboxScreen.js
App.js
...

## 🤔 Uso da geolocalização em apps reais

Alguns exemplos: rastreamento de entregas, mapas de calor de usuários, apps de visita, encontrar amigos próximos, serviços de emergência, turismo, etc.

## ⚠️ Desafios enfrentados

Integração entre WebView e APIs de mapas – lidar com tamanho dinâmico, injeção de HTML, permissões.

Persistência de localizações no Supabase – tratar lat/long como número, lidar com erros de rede, exibição de lista.

Compatibilidade de dependências com Expo – ajustar versões para evitar erro de compilação no Android.


## 🎬 Vídeo do app funcionando:
https://drive.google.com/drive/folders/11o7_9c78x1oCSktq1W2ouBrulQtU-Ql1

## 📊 Comparativo entre APIs de Mapas (Google Maps × Mapbox)
✅ Visão Geral

Google Maps é o veterano: simples de integrar, super preciso e cheio de recurso pronto.
Mapbox é o artista: permite personalizar tudo, estilizar e deixar o mapa com sua cara.

No geral:

Google Maps = praticidade + precisão
Mapbox = flexibilidade + visual top

## 🧩 Tabela Comparativa
| Critério | Google Maps | Mapbox |
|----------|-------------|--------|
| Facilidade de uso | ✅ Fácil | 🟡 Moderado |
| Precisão geográfica | ✅ Excelente | ✅ Alta |
| Personalização visual | 🔴 Limitado | ✅ Muito flexível |
| Performance | ✅ Ótima | ✅ Muito leve |
| Custos | 🟡 Free limitado | ✅ Free maior |
| Rotas / Navegação | ✅ Completo | 🟡 Básico |
| Suporte | ✅ Amplo | ✅ Bom |
| Offline | ❌ Não | ✅ Possível |
| Curva de aprendizado | Baixa | Média |
| Ideal para | Apps simples e rápidos | Apps personalizados |

## ✅ Pontos Fortes
🔹 Google Maps

Precisão absurda nas coordenadas

Integração rápida

Ecossistema gigante (Docs, exemplos, libs)

Ótimo para usar geocodificação + navegação

🔹 Mapbox

Total liberdade visual

Suporte a temas, camadas e estilos

Opção offline

Bom desempenho

## ⚠️ Pontos Fracos
🔸 Google Maps

Customização visual limitada

Custo pode subir dependendo do uso

Offline basicamente inexistente

🔸 Mapbox

Mais complexo de aprender

Funcionalidades de navegação mais simples

## ✅ Quando usar qual?
Cenário	Melhor escolha
Precisa só mostrar local	Google Maps
Quer rotas/endereços fáceis de implementar	Google Maps
Quer mapa estilizado para seu app	Mapbox
Precisa offline	Mapbox
Pouco tempo pra implementar	Google Maps
## 🏁 Conclusão

As duas APIs funcionam muito bem.
A escolha depende do foco do app:

✅ Google Maps → mais simples, rápido e preciso
✅ Mapbox → mais customizável e bonito

Se o objetivo é resultado rápido e funcional, vá de Google Maps.
Se você quer personalidade no design do mapa → Mapbox é o caminho.
