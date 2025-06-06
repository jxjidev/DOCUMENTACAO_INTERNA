# Apresentar erro no Programa

data: it\_teste type table of vbak, it\_teste1 type table of vbap.

data: w\_teste type vbak, w\_teste1 type vbap.

data: var\_soma type i.

select \* from vbak into table it\_teste.

var\_soma = 0. loop at it\_teste into w\_teste.

select \* from vbap into table it\_teste1. sort it\_teste1 by vbeln posnr.

loop at it\_teste1 into w\_teste1.

```
delete from vbap where vbeln = w_teste1-vbeln.
commit work.

add 1 to var_soma.

read table it_teste into w_teste with key vbeln = w_teste1-vbeln.
```

endloop.

endloop.
