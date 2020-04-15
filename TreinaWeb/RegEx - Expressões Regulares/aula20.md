# Casos típicos

## Casos típicosde RegEx: CPF
```
/^(?:[0-9]{3}\.){2}(?:[0-9]{3}\-)(?:[0-9]){2}$/gm
123.123.123-12
123.123.123-123
```

## Casos típicosde RegEx: CEP
```
/^(?:[0-9]){2}\.(?:[0-9]){3}\-(?:[0-9]){3}$/gm
11.111-111
11.111.111
11.111-1112
```

## Casos típicosde RegEx: datas
```
/^((?:[0-9]){2})\/((?:[0-9]){2})\/((?:[0-9]){4})$/gm
01/01/2001
02\02\2002

```

## Casos típicosde RegEx: emails
```
^(?:\w|-)+@(?:\w|-)+\.(?:com(?:\.br)?|net)$
mateusvilione@gmail.com
mateusvilione@gmail.com.br
a@a.com.br
mateus-vilione@gmail.com
mateus-vilione@gmail.net
matues_vilione599@hotmail.com
```

## Casos típicosde RegEx: telefones
```
^\([0-9]{2}\)\s9?[0-9]{4}\-[0-9]{4}$
(11) 1111-1111
(11) 91111-1111
```