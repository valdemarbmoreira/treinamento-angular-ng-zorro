# Angular
## Criar um novo projeto

Para criar um novo projeto 

```
ng new projeto-ng-zorro --prefix=app --style=less --no-standalone
```

## Instalar o ng zorro
Verificar versão do node

```
node -v
```

Verificar versão do angular-cli

```
ng --version
```

Lista de Compatibilidade entre Angular CLI, Node e Ng Zorro
Angular CLI:

| Versão do Angular | CLI	Node LTS compatível	| Versão do Ng Zorro compatível |
|-------------|-------------|-------------|
| 14.2.x |	16.14.x,18.x	| 14.x |
| 13.x	| 14.17.x, 16.x	| 13.x |
| 12.x |	12.22.x, 14.x	| 12.x |
| 11.x |	10.24.x, 12.x	| 11.x |
| 10.x |	8.16.x, 10.x |	10.x |

Para rodar 

```
ng serve
```

ou 

```
npm start
```

## Criar um novo componente

Para criar um novo componente

```
ng g c novo-componente
```

## Criar um nova diretiva

Para criar um nova diretiva

```
ng generate directive nome-da-sua-diretiva
```

## Criar um novo serviço

Para criar um nova diretiva

```
ng generate service nome-do-seu-servico
```

## Criar um novo interface

Para criar um nova interface

```
ng g i nova-interface
```

## Criar um novo modulo

Para criar um nova interface

```
ng g m novo-modulo
```

## Criar um novo modulo routing

Para criar um nova interface

```
ng g m novo-modulo-routing
```

Depois no arquivo

```
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';

const routes: Routes = [
  { path: '', redirectTo: 'dashboard', pathMatch: 'full' },
  {
    path: 'dashboard',
    loadChildren: () => import('./dashboard/dashboard.module').then(m => m.DashboardModule)
  },
  // Aqui você pode adicionar mais rotas principais conforme necessário
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

Não esquecer do 

```
<router-outlet></router-outlet>
```

e se o modulo routingo no filho trocar o ***forRoo***t para ***forChild***

## Criar um guarda de rota

Para criar um nova interface

```
ng s guard novo-guarda-rota
```

## Criar um pipe

Para criar um nova interface

```
Ng g p novo-pipe;
```

## Instalar ng zorro

Instalar a lib

```
npm install ng-zorro-antd@17.2.3
```

Configurar

```
ng add ng-zorro-antd
```

