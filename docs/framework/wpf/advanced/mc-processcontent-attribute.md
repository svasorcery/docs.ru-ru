---
title: Атрибут mc:ProcessContent
ms.date: 03/30/2017
helpviewer_keywords:
- mc:ProcessContent attribute
- XAML [WPF], mc:ProcessContent attribute
ms.assetid: 2689b2c8-b4dc-4b71-b9bd-f95e619122d7
ms.openlocfilehash: f7db71c065a04fb14216ffd08ca3b7c9d7cdf5af
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54673963"
---
# <a name="mcprocesscontent-attribute"></a>Атрибут mc:ProcessContent
Указывает, какие [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] элементы по-прежнему содержимое должно быть обрабатываемых соответствующих родительских элементов, даже если непосредственный родительский элемент может игнорировать [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] процессора из-за указания [mc: Ignorable-атрибут](../../../../docs/framework/wpf/advanced/mc-ignorable-attribute.md) . `mc:ProcessContent` Атрибут поддерживает совместимость разметки для пользовательского сопоставления пространства имен и [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] управления версиями.  
  
## <a name="xaml-attribute-usage"></a>Использование атрибута XAML  
  
```  
<object  
  xmlns:ignorablePrefix="ignorableUri"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix"...  
  mc:ProcessContent="ignorablePrefix:ThisElementCanBeIgnored"  
>  
    <ignorablePrefix:ThisElementCanBeIgnored>  
        [content]  
    </ignorablePrefix:ThisElementCanBeIgnored>  
</object>  
```  
  
## <a name="xaml-values"></a>Значения XAML  
  
|||  
|-|-|  
|*ignorablePrefix*|Любая строка допустимый префикс, согласно спецификации XML 1.0.|  
|*ignorableUri*|Любой допустимый URI для назначения пространства имен, согласно спецификации XML 1.0.|  
|*ThisElementCanBeIgnored*|Элемент, который может обрабатываться средством [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] реализаций обработчиков, если базовый тип не может быть разрешена.|  
|*[сведения]*|*ThisElementCanBeIgnored* помечается как игнорируемый. Если обработчик игнорирует этот элемент *[содержимое]* обрабатывается *объект*.|  
  
## <a name="remarks"></a>Примечания  
 По умолчанию [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] процессора будет игнорировать содержимое внутри игнорируемого элемента. Можно указать определенный элемент, `mc:ProcessContent`и [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] процессор будет продолжать обработку содержимого внутри игнорируемого элемента. Это обычно будет использоваться, если содержимое является вложенной в несколько тегов, по крайней мере один из которых является игнорируемым и по крайней мере один из которых не является игнорируемым.  
  
 Несколько префиксов может быть указан в атрибуте, используя разделитель, например: `mc:ProcessContent="ignore:Element1 ignore:Element2"`.  
  
 [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] Пространство имен определяет другие элементы и атрибуты, которые не документированы в этой области [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)]. Дополнительные сведения см. в разделе [спецификации совместимости разметки XML](https://go.microsoft.com/fwlink/?LinkId=73824).  
  
## <a name="see-also"></a>См. также
- [Атрибут mc: Ignorable](../../../../docs/framework/wpf/advanced/mc-ignorable-attribute.md)
- [Общие сведения о языке XAML (WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)
