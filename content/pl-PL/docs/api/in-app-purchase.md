# zakupy w aplikacji

> Zakupy w aplikacji w Mac App Store.

Proces: [Main](../glossary.md#main-process)

## Zdarzenia

Moduł `inAppPurchase` emituje następujące zdarzenia:

### Zdarzenie: 'transactions-updated'

Wyemitowane, gdy jedna lub więcej transakcji zostało zaktualizowanych.

Zwraca:

* `event` Event
* `transactions` ([Transaction[]](structures/transaction.md) - Tablica transakcji.

## Metody

Moduł `inAppPurchase` ma następujące metody:

### `inAppPurchase.purchaseProduct(productID, quantity, callback)`

* `productID` String - Identyfikator produktu do zakupu. (the id of `com.example.app.product1` is `product1`).
* `quantity` Integer (optional) - The number of items the user wants to purchase.
* `callback` Function (optional) - The callback called when the payment is added to the PaymentQueue. (You should add a listener with `inAppPurchase.addTransactionsListener` to get the transaction status). 
  * `isProductValid` Boolean - Sprawdź, czy produkt jest prawidłowy i czy został dodany do kolejki płatności.

### `inAppPurchase.canMakePayments()`

Zwraca wartość `Boolean`, niezależnie od tego, czy użytkownik może dokonać płatności.

### `inAppPurchase.getReceiptURL()`

Zwraca `String`, ścieżkę do paragonu.