# Doçuras.Ka · link na bio

Página do link na bio da [@docuras.ka](https://www.instagram.com/docuras.ka/), doceria artesanal em São José dos Pinhais – PR.

Quem clica na bio entende o que a Ka faz e escolhe um caminho:

- **Fazer meu pedido**: formulário curto para quem já sabe o que quer (nome, WhatsApp, pedido, data e retirada ou entrega).
- **Pedir orçamento**: formulário para festa, evento ou presente (ocasião, data, convidados, o que orçar, local e detalhes).
- **Ver o cardápio**: abre direto, sem formulário.

Os dois formulários montam a mensagem e abrem a conversa no WhatsApp da Ka com tudo organizado.

## Ver no computador

```bash
python3 -m http.server 8000
```

Depois abra http://localhost:8000.

## Antes de publicar

No começo do `<script>` do `index.html`:

| Constante | O que colocar |
| --- | --- |
| `PREVIA` | `false` (tira o selo "Prévia" e faz o formulário abrir o WhatsApp) |
| `WHATSAPP` | número da Ka, com 55 e DDD, só dígitos |
| `CARDAPIO_URL` | link do cardápio (PDF ou imagem; pode ficar em `assets/`) |
| `LEADS_URL` | opcional: para onde mandar os contatos (planilha ou Comercial do Boop Admin) |

Também falta:

- Fotos originais em alta resolução, com o mesmo nome em `assets/` (as atuais têm uns 500 px de largura).
- Confirmar com a Ka o nome para o bloco "Quem faz" e se ela faz entrega.

## Arquivos

- `index.html`: a página inteira, com estilo e script.
- `assets/`: fotos, logo, abelha, favicon e a fonte Bricolage Grotesque (servida pelo próprio site).
