# Individual Basic Note-taking C# App

## Description 

C# Note App, Individual App

Functionality (as of the first patch):

- You can create a project or a goal that you check (e.g., you track your progress in Genshin Impact, Summoners War, Elden Ring, whatever video game or business project).
- You can control your project according to the Permission and Roles system I designed.
- Security: I implement JWT auth to support my Permission system.

> I would like to point out that video games are a business project too. So, it applies to your projects.

## Objective

I would have to satisfy personal demand about the note-taking application and keep track of my progress, as well as to create visualization (charts, graphs, etc).

## How do you run my app (for the teacher/Developers)

### Cloning

The first step is to clone my repository:

```
git clone https://github.com/derweisskrag/ubiquitous-eureka.git
```

### .NET version

I would aim for the most recent .NET: 9.0. Why? I would use Entity Framework and SQLite from Microsoft.

### NuGet

You can run: 

```
dotnet restore
```

and then 

```
dotnet run
```

> Be careful! As you would use Microsoft VS Code Community Edition, you can run the app inside the VS code (Click on the Run Icon).
