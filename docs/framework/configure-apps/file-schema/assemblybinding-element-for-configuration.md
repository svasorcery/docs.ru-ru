---
title: '&lt;assemblyBinding&gt; элемент для &lt;конфигурации&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding
helpviewer_keywords:
- assemblyBinding Element
- <assemblyBinding> Element
ms.assetid: 6cc55983-b894-449b-8e26-b258e53939cd
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 64985d4ed2c6a82c54a7623df4b13d7ec54bff33
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54599352"
---
# <a name="assemblybinding-element-for-configuration"></a>\<assemblyBinding > элемент для \<configuration >

Определяет политику привязки сборок на уровне конфигурации.

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;**\<assemblyBinding >**

## <a name="syntax"></a>Синтаксис

```xml
<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
  <!-- Configuration files to include. -->
</assemblyBinding>
```

## <a name="attribute"></a>Атрибут

|           | Описание |
| --------- | ----------- |
| **xmlns** | Обязательный атрибут.<br><br>Задает пространство имен XML, необходимое для привязки сборок. Используйте строку urn:schemas-microsoft-com:asm.v1 в качестве значения. |

## <a name="parent-element"></a>Родительский элемент

|     | Описание: |
| --- | ----------- |
| [**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) | Корневой элемент в любом файле конфигурации, используемом средой CLR и приложениями .NET Framework. |

## <a name="child-element"></a>Дочерний элемент

|     | Описание |
| --- | ----------- |
| [**\<linkedConfiguration >**](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) | Указание файла конфигурации, который следует включить. |

## <a name="remarks"></a>Примечания

[  **\<LinkedConfiguration >** ](~/docs/framework/configure-apps/file-schema/linkedconfiguration-element.md) элемент упрощает управление сборки компонентов, позволяя файлы конфигурации в файлах конфигурации приложения, чтобы включить сборку хорошо известного расположения, а не дублировать параметры конфигурации сборки.

> [!NOTE]
>  **\<LinkedConfiguration >** элемент не поддерживается для приложений с манифестами side-by-side Windows.

## <a name="example"></a>Пример

Приведенный ниже показано, как включить файл конфигурации на локальном жестком диске:

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml" />
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a>См. также

- [Схема файла конфигурации для .NET Framework](~/docs/framework/configure-apps/file-schema/index.md)
