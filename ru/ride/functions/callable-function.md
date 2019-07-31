# Вызываемая функция

**Вызываемая функция** — [функция](/ride/functions.md) [dApp-скрипта](/ride/ride-script/dapp-script.md) с [аннотацией](/ride/annotations.md) `@Callable`.

У dApp-скрипта может быть несколько вызываемых функций.

Вызываемую функцию у [dApp](/blockchain/dapp.md) можно вызвать с помощью [транзакции вызова скрипта](/blockchain/transaction-type/invoke-script-transaction.md).

## Пример

``` ride
@Callable(inv)
func rate(name: String, rating: Int) = {
    WriteSet([DataEntry(inv.caller.toString(), name + rating.toString()])
}
```
