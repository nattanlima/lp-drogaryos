# LP Droga Ryos

Landing page estática (HTML + CSS + um pouco de JS). Sem build, sem dependências.

**Droga Ryos** — Avenida Bela Vista, QD. 35, LT. 23, Sala 3, Parque Trindade I,
Aparecida de Goiânia/GO, CEP 74921-206.
Pedidos e tele-entrega pelo WhatsApp (62) 98282-0284 · Todos os dias, 07h40–21h30.

Rede com outras unidades em Goiânia: Vila Nova (62) 98222-2170 · Vila Rizzo (62) 98282-0285.

> Projeto clonado de `nattanlima/lp-santamonica` e adaptado. O `.git` ainda aponta
> para o repositório original — rode `git remote remove origin` (ou reinicialize)
> antes de publicar em um repositório novo.

## Rodar localmente

```bash
npx http-server -p 8099
# abre http://localhost:8099
```

Ou simplesmente abra `index.html` no navegador.

## Estrutura

```
index.html               página inteira (conteúdo + SEO + schema.org)
css/style.css            estilos
design-system/tokens.css cores, fontes, espaçamentos
js/main.js               acordeão do FAQ + ano do rodapé
img/                     imagens (logo, hero, fachada, serviços, favicon)
```

Todos os botões de WhatsApp da unidade Parque Trindade I apontam para
`https://wa.me/5562982820284?text=vim%20pelo%20site%20preciso%20de%20atendimento`.
Para mudar o número ou a mensagem, troque em todos — é o mesmo link repetido.

## O que ainda falta confirmar antes de publicar

- **Domínio** — está com o placeholder `drogaryos.com.br` no `canonical`, no `og:url`,
  no `og:image`, no `schema.org` e no arquivo `CNAME`. Troque pelo domínio real.
- **Bairros de entrega** — na seção "Tele-Entrega" a lista ainda tem
  `[Bairro vizinho 1..5]`. Preencha com os bairros reais ou apague o `<ul class="chips">`.
- **Serviços** — a página afirma que a farmácia faz aferição de pressão, teste de
  glicemia e aplicação de injetáveis (você confirmou que são os mesmos serviços).
  As **3 fotos** desses cards (`servico-pressao/glicemia/injetaveis.webp`) foram
  baixadas de um site de referência e têm risco jurídico de banco de imagens —
  o ideal é trocar por fotos reais da loja.
- **Formas de pagamento** no FAQ (está "Pix, dinheiro e cartões").
- **Logo** — o favicon e os logos do hero/rodapé ainda usam o logo do template.
  Se a Droga Ryos tiver logo próprio, é só me mandar que eu substituo
  (`img/logo.webp`, `img/logo-branco.webp`, `img/favicon.png`, `img/apple-touch-icon.png`).

## Imagens

| Arquivo                   | Proporção | Uso                           |
|---------------------------|-----------|-------------------------------|
| `hero-farmaceutica.webp`  | 1600×1000 | Fundo do hero                 |
| `fachada.webp`            | 800×600   | Seção "Sobre" (fachada nova)  |
| `servico-pressao.webp`    | 600×400   | Card de pressão ⚠️ trocar     |
| `servico-glicemia.webp`   | 600×400   | Card de glicemia ⚠️ trocar    |
| `servico-injetaveis.webp` | 600×400   | Card de injetáveis ⚠️ trocar  |
| `logo.webp`               | 300×300   | Logo no hero                  |
| `logo-branco.webp`        | 260×260   | Logo no rodapé (fundo escuro) |
| `favicon.png`             | 96×96     | Ícone da aba do navegador     |
| `apple-touch-icon.png`    | 180×180   | Ícone para iOS/atalho         |
