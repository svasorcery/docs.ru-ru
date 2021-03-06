---
title: Вызов функций в запросах LINQ to Entities
ms.date: 03/30/2017
ms.assetid: 12a525a9-727c-4464-a0c7-71a0ef541792
ms.openlocfilehash: 012f55113cbea00c95c92712d640313a960ef8ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54542722"
---
# <a name="calling-functions-in-linq-to-entities-queries"></a>Вызов функций в запросах LINQ to Entities
В подразделах этого раздела описывается вызов функций в запросах LINQ to Entities.  
  
 Классы <xref:System.Data.Objects.EntityFunctions> и <xref:System.Data.Objects.SqlClient.SqlFunctions> обеспечивают доступ к каноническим функциям и функциям базы данных посредством платформы Entity Framework. Дополнительные сведения см. в разделе [Как Вызов канонических функций](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md) и [как: Вызов функций базы данных](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md).  
  
 Процесс вызова пользовательской функции состоит из трех основных шагов.  
  
1.  Определите функцию в концептуальной модели или объявите функцию в модели хранения.  
  
2.  Добавьте метод в приложение и сопоставьте его с функцией в модели с помощью <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute>.  
  
3.  Вызовите функцию в запросе LINQ to Entities.  
  
 Дополнительные сведения см. в подразделах этого раздела.  
  
## <a name="in-this-section"></a>В этом разделе  
 [Практическое руководство. Вызов канонических функций](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md)  
  
 [Практическое руководство. Вызов функций базы данных](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md)  
  
 [Практическое руководство. Вызов настраиваемых функций базы данных](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-custom-database-functions.md)  
  
 [Практическое руководство. Вызов определенных моделью функций в запросах](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-in-queries.md)  
  
 [Практическое руководство. Вызов определенных моделью функций как методов объектов](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-as-object-methods.md)  
  
## <a name="see-also"></a>См. также
- [Запросы в LINQ to Entities](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
- [Канонические функции](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
- [Обзор файла .edmx](https://msdn.microsoft.com/library/f4c8e7ce-1db6-417e-9759-15f8b55155d4)
- [Практическое руководство. Определения пользовательских функций в концептуальной модели](https://msdn.microsoft.com/library/0dad7b8b-58f6-4271-b238-f34810d68e5f)
