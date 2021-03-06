---
title: '&lt;Очистить&gt; элемент для NameValueSectionHandler и DictionarySectionHandler'
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName/clear
helpviewer_keywords:
- clear Element
- <clear> Element
ms.assetid: ff2294ec-fb82-4b0c-933e-ae185433fc7b
author: guardrex
ms.author: mairaw
ms.openlocfilehash: 55925ee5e9c5a17f14bd199125dbaacbadb9d928
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720945"
---
# <a name="clear-element-for-namevaluesectionhandler-and-dictionarysectionhandler"></a>\<Очистить > элемент для NameValueSectionHandler и DictionarySectionHandler

Удаляет все ранее определенные параметры в разделе.

[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md)   
&nbsp;&nbsp;[**\<параметра sectionName >**](~/docs/framework/configure-apps/file-schema/custom-element-2.md)   
&nbsp;&nbsp;&nbsp;&nbsp;**\<Очистить >**

## <a name="syntax"></a>Синтаксис

```xml
<clear />
```

## <a name="attributes"></a>Атрибуты

Нет

## <a name="parent-element"></a>Родительский элемент

|     | Описание: |
| --- | ------------|
| [**\<параметра sectionName >** элемент](~/docs/framework/configure-apps/file-schema/custom-element-2.md) | Определяет параметры для пользовательских разделов конфигурации, использующие <xref:System.Configuration.NameValueSectionHandler> и <xref:System.Configuration.DictionarySectionHandler> классы. |

## <a name="child-elements"></a>Дочерние элементы

Нет

## <a name="remarks"></a>Примечания

Можно использовать  **\<снимите >** элемент нужно удалить все параметры из приложения, которые были определены на более высоком уровне в иерархии файла конфигурации.

## <a name="example"></a>Пример

В этом примере определяются в файле конфигурации компьютера и файл конфигурации приложения и показано, как использовать  **\<снимите >** элемент в файле конфигурации приложения для очистки разделов, определенных ранее в файл конфигурации компьютера.

В коде следующего файла конфигурации компьютера объявляет разделе  **\<mySection >**:

```xml
<!-- Machine.config file -->
<configuration>
  <configSections>
    <section name="mySection" type="System.Configuration.NameValueSectionHandler,System" />
  </configSections>
  <mySection>
    <add key="key1" value="value1" />
    <add key="key2" value="value2" />
  </mySection>
</configuration>
```

В коде следующего файла конфигурации приложения удаляет все параметры из  **\<mySection >**. Приложение не может получить какие-либо параметры, которые были объявлены в в  **\<mySection >** раздел файла конфигурации компьютера.

```xml
<!-- Application configuration file -->
<configuration>
  <mySection>
    <clear/>
  </mySection>
</configuration>
```

## <a name="configuration-file"></a>файл конфигурации

Этот элемент может использоваться в файле конфигурации приложения, файл конфигурации компьютера (*Machine.config*), и *Web.config* файлы, которые не на уровне каталога приложения.

## <a name="see-also"></a>См. также

- [Схема файла конфигурации для .NET Framework](~/docs/framework/configure-apps/file-schema/index.md)
