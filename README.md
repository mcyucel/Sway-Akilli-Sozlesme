# Sway-Akilli-Sozlesme
Sway programlama dili ile yazılan akıllı sözleşme örneği

Sway, Fuel Network tarafından geliştirilen ve Ethereum Sanal Makinesi (EVM) ile uyumlu bytecode'a derlenebilen, Solidity'ye benzer bir programlama dilidir. Bu, Sway'in akıllı sözleşmeler geliştirmek için ideal bir dil olmasını sağlar. Sway programlama dili, Rust ile Solidity karışımı bir dildir diyebiliriz.

```sway
contract MyContract {

    // State değişkeni
    var balance: u64;

    // Fonksiyon
    fn deposit(amount: u64) {
        balance += amount;
    }

    // Olay
    event Deposited(amount: u64);

    // Fonksiyon
    fn withdraw(amount: u64) {
        if amount <= balance {
            balance -= amount;
            emit Deposited(amount);
        }
    }
}
```

Bu örnek, balance adında bir state değişkeni ve deposit ve withdraw adında iki fonksiyon içeren basit bir akıllı sözleşmedir. deposit fonksiyonu, sözleşmenin bakiyesine para yatırır ve withdraw fonksiyonu ise bakiyeden para çeker.
