# Week 4 — First Solana Program

## Цель
Целью задания было создать свою первую Solana Program на Rust, собрать её и задеплоить в сеть Devnet.

## Что делает программа
Программа содержит простую instruction, которая при вызове выводит сообщение в logs:

```text
Hello from Aisana Solana Program!
```

Это простая учебная программа, которая показывает базовую структуру Solana Program и работу с `entrypoint`.

## Использованные инструменты
В работе были использованы:

- Rust
- Solana CLI
- Solana Devnet
- Cargo
- cargo build-sbf
- Solana Explorer
- GitHub

## Основной код программы
Основной код находится в файле:

```text
src/lib.rs
```

В программе используется функция `process_instruction`, которая запускается при вызове программы.

Основная строка:

```rust
msg!("Hello from Aisana Solana Program!");
```

выводит сообщение в logs.

## Сборка программы
Для сборки Solana Program была использована команда:

```bash
cargo build-sbf
```

После успешной сборки в папке:

```text
target/deploy
```

были созданы файлы:

```text
week4_first_program.so
week4_first_program-keypair.json
```

Файл `.so` содержит скомпилированную программу, а `keypair.json` используется для Program ID.

## Program ID
Program ID созданной программы:

```text
4Cf2WPT4uX8bXPoMUs79ii3HbRwhAy59WhTexzJr6oGZ
```

## Деплой программы
Для загрузки программы в сеть Devnet использовалась команда:

```bash
solana program deploy target/deploy/week4_first_program.so
```

Программа была успешно задеплоена.

## Deploy Signature
Signature транзакции деплоя:

```text
B1d9rYuuPJFxkDQkmK4yXsJruqfVBp4UqCibWMMTmHcG2q86n1RRLg2JEMdZG3SSCtbMiNyw6LczAcATzP3aWjk
```

## Проверка программы
Для проверки информации о программе использовалась команда:

```bash
solana program show 4Cf2WPT4uX8bXPoMUs79ii3HbRwhAy59WhTexzJr6oGZ
```

## Solana Explorer
Ссылка на программу в Solana Explorer:

https://explorer.solana.com/address/4Cf2WPT4uX8bXPoMUs79ii3HbRwhAy59WhTexzJr6oGZ?cluster=devnet

Ссылка на транзакцию деплоя:

https://explorer.solana.com/tx/B1d9rYuuPJFxkDQkmK4yXsJruqfVBp4UqCibWMMTmHcG2q86n1RRLg2JEMdZG3SSCtbMiNyw6LczAcATzP3aWjk?cluster=devnet

## Результат
В результате была создана первая Solana Program на Rust.

Программа успешно собралась с помощью `cargo build-sbf` и была задеплоена в сеть Devnet.

После деплоя был получен Program ID и Signature транзакции.

## Вывод
В ходе выполнения задания я познакомилась с базовой структурой Solana Program, сборкой SBF-программы и процессом деплоя в Devnet.

Также я научилась получать Program ID, проверять программу через Solana CLI и находить её в Solana Explorer.