# [samosqscript](http://www.sistemasamo.com)
Biblioteca desenvolvida em javascript para melhorar o desenvolvimento de script SQlite em ferramenta Online e Offline

## Como usar
Inclua na tag `head` o seguinte código `<script type="text/javascript" src="com.sistemasamo.js"></script>`

## Exemplos do biblioteca
* Inicialização
* Select
* Insert
* Update
* Delete
* Joins
* Create Table
* Modify Table
* 

## Inicialização
`var objDatabase = new sqlLite();`

## Select
```
objDatabase.get('*');
objDatabase.table('finance_bank');
objDatabase.where('bank_sinc', '!=', 3);
objDatabase.where('substr(bank_date, 0, 8)', '=', '2015-09');
objDatabase.order({bank_date:'asc'});
objDatabase.select(function(resultado, total, linha){
  alert(resultado.bank_uid +'<>'+ resultado.bank_title);
}
```

## Insert
```
objDatabase.set({
    bank_uid                 : data.lancamentos[i].bank_uid,
    bank_account             : data.lancamentos[i].account_uid,
    bank_category            : data.lancamentos[i].category_uid,
    bank_sinc                : 0
});
objDatabase.table('finance_bank');
objDatabase.insert();
```

## Update
```
var updateBasico = {
    bank_typer      : bank_typer,
    bank_date       : bank_date,
    bank_description: bank_description,
    bank_value      : bank_value,
    bank_account    : bank_account,
    bank_category   : bank_category,
    bank_paid       : bank_paid
};

objLancamento.table('finance_bank');
objLancamento.set(updateBasico);
objLancamento.where({bank_uid: codigoEdicao});
objLancamento.update(function(){
    location.href = 'principal.html?'+time();
});
```



