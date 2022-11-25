# LarryGitHub

1. Qué comando utilizaste en el paso 11?
   - `git reset --hard HEAD~01`

   - Por qué? para asegurar borrarlo del working copy

2. Qué comando o comandos utilizaste en el paso 12?
   
   - `git reflog` -> para ver una lista de los movimientos de el puntero `HEAD` y así identificar el commit ID que queria restuarar

   - `git reset <commit_ID>` en mi caso `git reset 5aa6f2f` para deshacer el commit y dejar los cambios de ese commit en el working copy

   - `git restore git-nuestro.md` para moverlo al area repositorio y recuperar el commit anteriormente borrado

3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 
  
  -  No puesto que la branch fue creada con base en `master` (en mi caso `main`)

4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

   - Si, porque los commits de ambas ramas `styled` and `hmtlify` modificaban lineas en comun con diferente contenido 

5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

    - No. Este era un merge fast-forward, que era basicamente adicionar los últimos commits de `styled`, los commits anteriores era el mismo contenido de `master` (`main` en mi caso) 

6. ¿Qué comando o comandos utilizaste en el paso 25?

- Normalmente se usa `git log --graph`
- Yo me encontre este con decorados y colorcitos

   `git log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all`

   Así que me adicioné un alias, nadie se acuerda de esa chorrera 😬

   `git config --global alias.graph "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all"`

7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

- Si La rama title era master(main) con un commit de direferencia. Así que Git podia automaticamente adicionar ese commit de diferencia y mover el puntero a ese ID sin problema.

8. ¿Qué comando o comandos utilizaste en el paso 27?

   En este case se puede `git reset HEAD~02` o `git reset b5e0074` con el commit ID previo al merge

9. ¿Qué comando o comandos utilizaste en el paso 28?

   `git restore git-nuestro.md`

10. ¿Qué comando o comandos utilizaste en el paso 29?

   `git branch -D title`

11. ¿Qué comando o comandos utilizaste en el paso 30?

   `git reflog` y luego `git reset `

12. ¿Qué comando o comandos usaste en el paso 32?

13. ¿Qué comando o comandos usaste en el punto 33? 