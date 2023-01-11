## TypeScript

- TypeScript é uma linguagem de programação e um superset do JavaScript. O Typescript permite que seja adicionado uma camada de tipagem ao JavaScript, em função de manter o código com menos error e que tenha uma fatoração mais simples.

## Rodando TypeScript

- Faça instalação do TypeScript globalmente
- Inicialize uma nova aplicação node
    
    ```powershell
    # inicializar projeto node 
    npm init --y 
    
    #Instalar dependencia Typescript
    npm i -D typescript 
    
    npm i -D tc-node-dev
    
    npm i -D ts-node
    
    # Inicializar typescript no projeto
    npx tsc --init
    
    # Transpilar arquivo ts para js
    tsc file.ts 
    
    # Rodando com extenção (configure antes)
    npx ts-node file.ts 
    
    ```
    

## Função sem typagem vs com typagem

- Sem tipagem

```jsx
const soma = (a, b) => {
	consele.log(a+b)
}

soma(2, 2)
```

- Com tipagem

```tsx
const soma = (a: number, b: number) => {
	console.log(a+b)
}

soma(2, 2) // Requer type number
```
