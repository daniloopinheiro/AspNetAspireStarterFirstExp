[FONTE:](https://learn.microsoft.com/pt-br/dotnet/aspire/fundamentals/setup-tooling?tabs=dotnet-cli#install-net-aspire)
# Primeiro Experimento com AspNet Aspire Starter

## Antes de executar

> Para trabalhar com o .NET Aspire, você precisará das seguintes instalações localmente:

```
- .NET 8.0
- Carga de trabalho do .NET Aspire:
  - Usar o instalador do Visual Studio
```

> Use o comando dotnet workload install aspire

```shell
$ dotnet workload update
$ dotnet workload install aspire
$ dotnet workload list
```
```
- Área de Trabalho Docker: https://www.docker.com/products/docker-desktop/
- Ambiente de desenvolvedor integrado (IDE) ou editor de código, como:
  - Visual Studio 2022 Preview versão 17.9 ou superior (opcional)
  - Código do Visual Studio (opcional)
```

## Modelos de projeto do Aspire

Atualmente existem dois modelos de projeto disponíveis:

- Aplicativo .NET Aspire: um aplicativo .NET Aspire mínimo que inclui o seguinte:
  - AspireSample.AppHost: Um projeto orquestrador projetado para conectar e configurar os diferentes projetos e serviços do seu aplicativo.
  - AspireSample.ServiceDefaults: um projeto compartilhado do .NET Aspire para gerenciar configurações que são reutilizadas nos projetos da sua solução relacionados à resiliência, descoberta de serviços e telemetria.

- Aplicativo .NET Aspire Starter: Além dos projetos .AppHost e .ServiceDefaults, o aplicativo .NET Aspire Starter também inclui o seguinte:
  - AspireSample.ApiService: um projeto de API ASP.NET Core Minimal é usado para fornecer dados ao frontend. Este projeto depende do projeto AspireSample.ServiceDefaults compartilhado.
  - AspireSample.Web: um projeto ASP.NET Core Blazor App com configurações de serviço .NET Aspire padrão, este projeto depende do projeto AspireSample.ServiceDefaults.

Use o Visual Studio ou a CLI do .NET para criar novos aplicativos usando esses modelos de projeto. Explore modelos de projeto adicionais do .NET Aspire no repositório de exemplos do .NET Aspire.

```shell
$ dotnet new list aspire
```

> Para criar um projeto .NET Aspire básico:

```shell
$ dotnet new aspire
```

> Para criar um projeto .NET Aspire com uma UI e API de amostra incluídas:

```shell
$ dotnet new aspire-starter
```

### Projeto do repositório

> Criação do projeto

```shell
$ dotnet new aspire-starter --use-redis-cache --output AspNetAspireStarterFirstExp
```

> Execução do projeto

```shell
$ dotnet run --project AspNetAspireStarterFirstExp/AspNetAspireStarterFirstExp.AppHost
```
