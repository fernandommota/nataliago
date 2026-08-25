# nataliago.med.br

Site institucional da Dra. Natália T. Borato Maia — ginecologia e obstetrícia.

HTML e CSS estáticos, sem build step e sem dependências. Dois HTML, um CSS,
~15 linhas de JS inline. A única requisição externa é o Google Fonts.

## Rodar

```sh
python3 -m http.server 8000
```

## Estrutura

```
index.html            one-page — todo o conteúdo
template-pagina.html  esqueleto de página satélite (copiar e renomear)
styles.css            CSS único, tokens em :root
assets/               favicon, og:image e as 4 fotos em .webp
CNAME .nojekyll robots.txt sitemap.xml
```

Seções do `index.html`, na ordem: hero, credenciais, `#sobre`,
`#atendimentos`, `#consulta`, citação, `#artigos`, `#duvidas`, `#contato`.

## Convenções

- **Header e footer são duplicados** entre os dois HTML — é o preço de não ter
  build step. Ao mexer na navegação, atualizar os dois.
- **Imagens entram pré-recortadas** na proporção da caixa de destino
  (4:5 no hero, 3:4 em `#sobre`, 1:1 em `#consulta`). Nenhuma usa
  `object-position`.
- **O menu tem breakpoint próprio em 1080px**, maior que o de layout em 960px:
  com 6 itens + CTA a folga acaba perto de 1000px. Ao incluir item no menu,
  remedir antes de publicar.
- **O JSON-LD espelha o HTML visível** — telefone, endereço e horários mudam
  nos dois lugares.
- **CRM e RQE ficam visíveis** no header e no rodapé: exigência do CFM.

## Deploy

GitHub Pages servindo a raiz do `main`. Em **Settings → Pages**: source
*Deploy from a branch*, `main`, `/ (root)`; o domínio vem do `CNAME`.

DNS no registro.br — apex com quatro registros **A** para
`185.199.108.153`, `.109.153`, `.110.153` e `.111.153`, e `www` como **CNAME**
para `fernandommota.github.io.`

---

Pendências de conteúdo, dados profissionais, conformidade CFM e notas técnicas
detalhadas estão em `CONTEUDO.md` — documento interno, fora do versionamento.
