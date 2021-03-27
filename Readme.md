# Paket Publish Issue Example

When publishing a basic Asp.Net 5 application and using NuGet, all dependencies
are correctly included in the publish folder.

However, when using Paket, dependent packages are missing. 

This repo contains two branches:
* Main: Showcasing the working NuGet example,
* Paket: Showcasing the broken version when using Paket.

As a simple example, only one Package (Autofac) is included and used in Program.cs

Comparing the publish folder from the Paket branch with the Nuget Branch shows 
clearly that Autofac.dll is missing.

Simply run: `dotnet publish -r win-x64 -c Debug -f net5.0`

This was tested on the following environment: 
* OS: Windows 10,
* .Net SDK: 5.0.201
* Paket: 6.0.0-beta8