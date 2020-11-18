# apisdn 1.0
API - SALA DA NOTÍCIA

# Class Sdn
##---------------------------- STATUS DA API

> Verifica se o token/api está disponível para o domínio

```
use Sdn;

$SDN = new Sdn;
$api = $SDN->statusApi();
echo $api['label']; // utilize essa função para verificar a saúde do seu token ou da api.
```

##---------------------------- RETORNO DO RELEASE PUBLICADO

> É obrigatório informar a URL publica do release assim que importado

```
$retorno = $this->retorno($releaseId,$url_gerada);

if($retorno['status']==200 and $retorno['json_d']['status']=='success'){
                    
      $retornostatus      = $retorno['json_d']['status'];
      $retornostatus_logs = $retorno['json_d']['status_logs'];
}
```

##---------------------------- LISTAR EDITORIAS
```
$this->getCategorias([]);
```
##---------------------------- LISTAR REGIÕES
```
$this->getRegioes([]);
```
##---------------------------- GET NAME EDITORIA
```
$this->getNameEditoria(ID_EDITORIA);
```
##---------------------------- GET LIST RELEASES
```
$this->getReleases([]);
```
##---------------------------- GET RELEASE POR ID
```
$this->getReleaseId(ID_RELEASE);
```

##----------------------------


# REQUESTS HTTP 

##---------------------------- Get Releases Lista

https://urldaapi.com.br/api/1.0/releases/TOKEN/listar/FILTRO/LIMITE/ORDER/PAGE

FILTRO = ALL => todos ||| EDITORIA|REGIAO|TRUE => 1|1|TRUE OR FALSE = com/sem foto

LIMITE = 50

ORDER = data_desc data_asc data_atualizacao_desc data_atualizacao_asc

PAGE = 1


##---------------------------- Get Editorias Lista

https://urldaapi.com.br/api/1.0/releases/TOKEN/editorias/ALL/LIMITE/ORDER/PAGE

FILTRO = ALL => todos

LIMITE = 50

ORDER = id_desc nome_desc nome_asc

PAGE = 1

##---------------------------- Get Regiões Lista

https://urldaapi.com.br/api/1.0/releases/TOKEN/regioes/ALL/LIMITE/ORDER/PAGE

FILTRO = ALL => todos

LIMITE = 50

ORDER = id_desc id_asc nome_desc nome_asc

PAGE = 1

##---------------------------- Get Editoria

https://urldaapi.com.br/api/1.0/releases/TOKEN/geteditoria/ID_EDITORIA

ID_EDITORIA = ID da editoria

##---------------------------- Get Release

https://urldaapi.com.br/api/1.0/releases/TOKEN/get/ID_RELEASE

ID_RELEASE = ID do release

##---------------------------- Retorno Release 

https://urldaapi.com.br/api/1.0/releases/TOKEN/retorno/ID_RELEASE

ID_RELEASE = ID do release

enviar POST[noticia_url] = URL da notícia gerada no Portal/Plataforma

Retorno Success = HTTP 200

Retorno Erro = HTTP 404

