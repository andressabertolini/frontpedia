Digite no terminal:

```jsx
git rebase -i HEAD~5
```

Isso vai pegar os 5 últimos commits, menos o atual e vai mostrar numa lista

Dai você vai navegar pelas setas pra cima e pra baixo nessa lista, e vai digitar d e dar enter naqueles que você quiser apagar. Não pode apagar todos da lista, tem que deixar pelo menos 1

Quando terminar, digite :wq e enter

Dai pra forçar pra mandar pro repositório (ele vai querer puxar os commits antigos de volta, use:

```jsx
git push —force origin mater
```