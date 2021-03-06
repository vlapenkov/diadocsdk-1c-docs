﻿GetDocumentEventList
====================

Метод объекта :doc:`Organization <Organization>`

**Синтаксис**


GetDocumentEventList(<EventId>)

**Параметры**


-  <EventId> (cтрока, обязательный) идентификатор последнего полученного события или пустая строка.

**Возвращаемое значение**


Коллекция :doc:`Collection <Collection>` объектов :doc:`DocumentEvent <DocumentEvent>`.

**Описание**


Возвращает список событий, следующих за событием с идентификатором EventId в хронологическом порядке, при этом само событие с идентификатором EventId в этот список не включается.
Если в качестве EventId передана пустая строка, то метод вернет самые старые события из ящика организации (начало истории изменений в ящике).
Если список событий содержит более 100 элементов, то в ответе возвращаются первые 100 элементов.
Предполагается, что интеграционное решение будет хранить идентификатор последнего полученного события EventId для получения списка следующих событий.
