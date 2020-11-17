# apisdn
API - SALA DA NOTÍCIA

##---------------------------- STATUS DA API

$SDN = new Sdn;

$api = $SDN->statusApi();

echo $api['label'];

##---------------------------- IMPORTAR RELEASE

$posicao = 'Posição da notícia em seu portal, configuração opcional'

$view = $SDN->cadastrarNoticia(["id_release"=>$id_release,"id_cat"=>$id_categoria_local,"posicao"=>$posicao]);
    
echo $view['msg'];
