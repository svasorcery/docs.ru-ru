### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>Значения NULL операции объединения отображаются в отладчике с запаздыванием на один шаг

|   |   |
|---|---|
|Подробные сведения|Из-за ошибки в .NET Framework 4.5 значения, заданные с использованием операции объединения NULL, не отображаются в отладчике немедленно после выполнения операции присваивания в 64-разрядной версии платформы.|
|Предложение|После выполнения одного дополнительного шага в отладчике локальные значения или значения поля корректно обновляются. Эта проблема также была устранена в .NET Framework 4.6 и может быть решена путем обновления до этой версии платформы.|
|Область|Пограничный случай|
|Версия|4.5|
|Тип|Среда выполнения|

