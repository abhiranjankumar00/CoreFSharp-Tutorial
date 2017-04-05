# Getting Started with .NET Core using F#

- Reference: [Youtube: Getting Started with .NET Core using F#](https://www.youtube.com/watch?v=2xG31sUsCdc)
- Uses [Kestrel web server](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/servers/kestrel)

## Prerequisites

- Install _.net core_.
- Install a editor. Preferably [VS Code](https://code.visualstudio.com/)
  - If using _VS Code_, extensions following packages:
    - [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp)
    - [C#](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)
    - [Optional] [Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim) (for vim users), [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons) (fancy icons)

## Build Steps

- Restore packages - `dotnet restore`
- Build project - `dotnet build`
- Launch webserver - `cd CoreFSharp.Web; dotnet run`

## Steps to create a project

- Create the top level project directory. We will use _CoreFSharp_ directory for it. It should be same as project name.
    - `mkdir CoreFSharp`
    - `cd CoreFSharp`
- **Create solution File:** `dotnet new sln`
- **Create a mvc subproject:**
    - Create the sub-directory first. `mkdir CoreFSharp.Web; cd CoreFSharp.Web`
    - Initialize sub-project: `dotnet new mvc -lang f#`
- **Reference subproject in solution file:** `dotnet sln add ./CoreFSharp.Web/CoreFSharp.Web.fsproj`
    - Verify it by calling `dotnet sln list`

## Extra info
- To check _.net core version_: `dotnet --version`
- List subprojects referenced in solution file (execute it from project root directory): `dotnet sln list`
- Files to be considered in .gitignore: _*/bin_, _*/obj_, _*.swp_, _*/wwwroot_
