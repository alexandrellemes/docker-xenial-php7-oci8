Docker PHP (com OCI8 driver)

Usage
=====

No seu arquivo Dockerfile, utilize a referencia a seguir para montar a sua imagem:

```
    FROM alexllid/xenial-php7-oci8
```

Importante
=========

Ao rodar o container baseado nessa image, o `$HOME/discoDocker/oracle/etc/tnsnames.ora` tem que ser informado utilizando a flag `-v`:

```
    docker run -v $HOME/discoDocker/oracle/etc/tnsnames.ora:/etc/tnsnames.ora alexllid/xenial-php7-oci8
```

Dentro da pasta `oracle/etc` tem um arquivo `tnsnames.ora` como exemplo.
