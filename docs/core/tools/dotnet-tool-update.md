---
title: Команда dotnet tool update
description: Команда dotnet tool update обновляет указанное глобальное средство .NET Core на вашем компьютере.
ms.date: 05/29/2018
ms.openlocfilehash: 2716f7f88ffe364bebacf970d7152f5509edc888
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169746"
---
# <a name="dotnet-tool-update"></a>dotnet tool update

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a>name

`dotnet tool update` обновляет указанное [глобальное средство .NET Core](global-tools.md) на компьютере.

## <a name="synopsis"></a>Краткий обзор

```console
dotnet tool update <PACKAGE_NAME> <-g|--global> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <PACKAGE_NAME> <--tool-path> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <-h|--help>
```

## <a name="description"></a>Описание

Команда `dotnet tool update` предоставляет способ обновления глобального средства .NET Core на компьютере до последней стабильной версии пакета. Команда удаляет и повторно устанавливает средство, эффективно обновляя его. Чтобы использовать эту команду, укажите, что хотите обновить средство из установки уровня пользователя с помощью параметра `--global`, или укажите путь к месту установки средства с помощью параметра `--tool-path`.

## <a name="arguments"></a>Аргументы

`PACKAGE_NAME`

Имя или идентификатор пакета NuGet, который содержит глобальное средство .NET Core, которое вы хотите обновить. Найти имя пакета можно с помощью команды [dotnet tool list](dotnet-tool-list.md).

## <a name="options"></a>Параметры

`--add-source <SOURCE>`

Добавляет дополнительный источник пакета NuGet для использования во время установки.

`--configfile <FILE>`

Файл конфигурации NuGet (*nuget.config*), который будет использоваться.

`--framework <FRAMEWORK>`

Указывает [требуемую версию .NET Framework](../../standard/frameworks.md) для обновления средства.

`-g|--global`

Указывает, что обновление предназначено для средства уровня пользователя. Не может использоваться вместе с параметром `--tool-path`. Если вы не укажете этот параметр, укажите параметр `--tool-path`.

`-h|--help`

Выводит краткую справку по команде.

`--tool-path <PATH>`

Указывает место установки глобального средства. Путь может быть абсолютным или относительным. Не может использоваться вместе с параметром `--global`. Если вы не укажете этот параметр, укажите параметр `--global`.

`-v|--verbosity <LEVEL>`

Задает уровень детализации команды. Допустимые значения: `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` и `diag[nostic]`.

## <a name="examples"></a>Примеры

Обновляет глобальное средство [dotnetsay](https://www.nuget.org/packages/dotnetsay/):

`dotnet tool update -g dotnetsay`

Обновляет глобальное средство [dotnetsay](https://www.nuget.org/packages/dotnetsay/), расположенное в определенной папке Windows:

`dotnet tool update dotnetsay --tool-path c:\global-tools`

Обновляет глобальное средство [dotnetsay](https://www.nuget.org/packages/dotnetsay/), расположенное в определенной папке Linux/macOS:

`dotnet tool update dotnetsay --tool-path ~/bin`

## <a name="see-also"></a>См. также

* [Глобальные средства .NET Core](global-tools.md)