# Функция-верификатор

**Функция-верификатор** — [функция](/ride/functions.md) [dApp-скрипта](/ride/ride-script/dapp-script.md) с [аннотацией](/ride/annotations.md) `@Verifier`.

Функция-верификатор отвечает за [валидацию транзакций](/blockchain/transaction-validation.md) и ордеров, которые отправляются с [dApp](/blockchain/dapp.md).

У dApp-скрипта может быть только _одна_ функция-верификатор.

Функция-верификатор не имеет аргументов.

## Пример

``` ride
@Verifier(tx)
func verify() = {
    match tx {
        case _: Order|SetScriptTransaction =>
            sigVerify(tx.bodyBytes, tx.proofs[0], tx.senderPublicKey)
        case _ => false
    }
}
```
