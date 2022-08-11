# Тестовое задание

## Общее описание

Проект представляет из себя аукцион, на который можно выставить токены NFT стандарта ERC-721. Каждый токен содержит в себе уникальный контент закодированный в строке, который может установить каждый пользователь при чеканке. На минт токенов установлен лимит - на 1 кошелек доступен только 1 токен. К эмиссии доступно 1111 токен - это максимальное количество токенов в коллекции. В проекте присутствуют whitelist и blacklist. Пользователям, входящим в белый список, доступна чеканка по более выгодным ценам. Пользователям в черном списке не доступны практически никакие операции с токенами коллекции. Контракты токена и аукциона являются обновляемыми, что позволит в будущем внести изменения при обнаружении уязвимостей.

## Описание процесса ставок
Чтобы принять участие в аукционе, необходимо отчеканить себе токен. После этого появляется возможность выставить его на аукцион. Во время аукциона невозможно отправить этот токен кому-либо, чтобы разблокировать его, необходимо снять токен с аукциона. Любой желающий может приобрести токен либо по стартовой цене (если не сделана ставка), либо сделать ставку, которую может принять продавец. Если покупатель приобретает токен по стартовой цене, его токены сразу отправляются на адрес продавца (за исключением комиссии в 3%), взамен он получает токен. Если покупатель хочет сделать ставку, а продавец ее принимает, токен отправляется на контракт Treasury, где сделка ожидает подтверждения обеих сторон и оплаты со стороны покупателя. Максимальное время ожидания оплаты - 1 час. После этого токен отправляется продавцу, а покупатель теряет возможность оплатить сделку. После того, как покупатель вызвал функцию оплаты в контракте Treasure, он может подтвердить сделку и получить свой токен. Продавец тоже может подтвердить сделку и получить свою оплату (за исключением комиссии 2%). Проценты подобраны так, чтобы простимулировать активные торги, ведь в таком случае комиссия будет меньше.

## Адреса контрактов
Все контракты развернуты и верифицированы в сети Goerli:
 - blacklist address:  0x8f141545F87127183F012921A4d45eaE401F5c7B
 - assets address:  0x25Dac87dc02a30c64881961714acCF2aA73cA8D3
 - treasury address:  0xE591C8F4b54eCAfc99A8B55A0b98B3D8bfBf04cc
 - auction address:  0xdc7b929D89EA0E1d0df55223A4d5dB3BC5714CD6
