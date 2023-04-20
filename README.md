# testuuid

есть идентификатор типа UUID (такие идентификаторы часто встречаются в работе), пример такого идентификатора:
123e4567-e89b-12d3-a456-426655440000
(могут быть цифры и символы от 'a' до 'f', символы в группах, группы разделены дефисами)

Чтобы отличить в базе данных сущности с такими идентификаторами созданные автотестами от сущностей созданных пользователями, надо перед созданием сущности поменять первую группу символов идентификатора на 'autotest',
т.е. в результате идентификатор должен стать таким:
autotest-e89b-12d3-a456-42665544fabc

Итого:
Надо реализовать функцию, которая будет возвращать строку идентифкатор, созданную из UUID, первая группа символов которого будет autotest

получить UUID для работы можно так:
import uuid
identificator = uuid.uuid4()

механизмов самой замены символов в строке несколько, будет хорошо, если решите двумя способами :)
