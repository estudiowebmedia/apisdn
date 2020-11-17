# apisdn 1.0
API - SALA DA NOTÍCIA

##---------------------------- STATUS DA API
/* Verifica se o token/api está disponível para o domínio */

$SDN = new Sdn;

$api = $SDN->statusApi();

echo $api['label'];


##---------------------------- RETORNO DO RELEASE PUBLICADO

$retorno = $this->retorno($releaseId,$url_gerada);

if($retorno['status']==200 and $retorno['json_d']['status']=='success'){
                    
      $retornostatus      = $retorno['json_d']['status'];
      $retornostatus_logs = $retorno['json_d']['status_logs'];
}

