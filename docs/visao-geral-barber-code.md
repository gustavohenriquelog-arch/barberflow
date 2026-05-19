### Duplicidade no gatilho da Branch prd e main ###


No bloco on.push.branches, você listou tanto main quanto prd. No seu passo de determinar o ambiente, você colocou que ambas apontam para ENVIRONMENT=prd.
Se a sua branch de produção for a main, você deve remover a prd do gatilho (ou vice-versa) para evitar disparos duplicados desnecessários se você mantiver as duas vivas.
