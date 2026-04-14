# AGENDA-ELITE-I2

Painel de gestão de eventos da consultoria **Seja AP** contratada pela i2Fibra.

## O que é este projeto

Agenda de cursos e eventos de desenvolvimento da equipe i2 ao longo de 2026.
Hospedada no GitHub Pages para acesso via link público (sem arquivo local).

**Link público:** https://i2-fibra.github.io/agenda-elite-i2/

## Arquivo principal

`index.html` — painel HTML completo com:
- **Aba Online**: eventos online por mês (GAP, RH, Comercial, Marketing, IA, Hot Seat, Treinamento, Conexão)
- **Aba Presencial**: APNs, encontros e formações presenciais
- **Aba Conflitos**: detecção automática de sobreposições de horário
- **Aba Por Pessoa**: visão individual de cada colaborador com todos os cursos e aulas
- **Aba Eliteens**: programa para filhos de colaboradores

## Pessoas na agenda

Gabriel (CEO), Cleire (Sócia), Weslley, Rafael, Gustavo, Rubens, Pedro,
Josias, Laysla, Patrick, Maria, Hugo, Janderson, Vitoria, Erika,
Victor Hugo, Francieli, Leonilda, Andressa, Claudia, Vitor Martins

## Como fazer alterações

Chame o Claude Code nesta pasta e diga o que precisa:
- "Fulano faltou na Aula X de [curso]" → atualiza presença
- "Muda participantes do evento [X]" → edita o array de eventos
- "Adiciona novo evento em [data]" → insere no array EO ou EP
- "Reorganiza [curso] para todo mundo participar" → redistribui participantes

Após qualquer alteração, o Claude commita e faz push automaticamente → GitHub Pages atualiza em ~1 min.

## Estrutura de dados no HTML

- `EO[]` — eventos online
- `EP[]` — eventos presenciais
- `PESSOAS{}` — mapa de pessoa → cursos → aulas (com datas)
- `ELITEENS_DATA[]` — eventos do programa Eliteens

## Protocolo de sessão

### Iniciar sessão
```
/iniciar-sessao
```

### Fechar sessão
```
/fechar-sessao
```
