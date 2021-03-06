# Транзакция

**Транзакция** — действие на [блокчейне](/blockchain/blockchain.md) от имени [аккаунта](/blockchain/account.md).

Транзакции можно отправлять _только_ с аккаунта — таким образом, любую транзакцию можно соотнести с каким-либо аккаунтом.

Cуществует несколько [типов транзакций](/blockchain/transaction-type.md).

## ID транзакции <a id="transaction-id"></a>

У каждой транзакции есть уникальный ID.

**ID транзакции** — хеш от [байтов тела транзакции](/blockchain/transaction-body-bytes.md), который вычисляется хеш-функцией [blake2b256](https://en.wikipedia.org/wiki/BLAKE_&#40;hash_function&#41;).

В отличие от остальных типов транзакций, ID [транзакции создания псевдонима](/blockchain/transaction-type/alias-transaction.md) рассчитывается как хеш от значений полей `type` и `alias`.

## Временная метка транзакции <a id="transaction-timestamp"></a>

**Временная метка транзакции** — приблизительное время отправки транзакции в [сеть блокчейна](/blockchain/blockchain-network.md).

Фактическое время отличается от значения временной метки не более чем на 2 часа назад и 1,5 часа вперед.

Время указано в миллисекундах, которые прошли с начала [эпохи Unix](https://ru.wikipedia.org/wiki/Unix-время).

## Бинарный формат

Смотрите страницу [Бинарный формат транзакции](/blockchain/binary-format/transaction-binary-format.md).
