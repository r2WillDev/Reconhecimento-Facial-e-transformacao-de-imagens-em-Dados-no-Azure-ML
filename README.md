# Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML

O **Azure AI Vision** inclui vários recursos para entender o conteúdo e o contexto da imagem e extrair informações de imagens. O Azure AI Vision Studio permite que você experimente muitos dos recursos de análise de imagem.
Neste exercício, você usará o Vision Studio para analisar imagens usando as experiências de teste integradas.

## Criar um recurso de serviços de IA do Azure
Você pode usar os recursos de análise de imagem do Azure AI Vision com um recurso multisserviço dos **serviços de IA do Azure**. Se você ainda não tiver feito isso, crie um recurso de **serviços de IA do Azure** em sua assinatura do Azure.

> [!NOTE]
> Caso não tenha um resource group criado, siga o primeiro passo a passo no repositorio sobre [Machine Learning](https://github.com/r2WillDev/LAB-MachineLearning-Azure-ML)

1. Entre no portal do [Azure]( https://portal.azure.com) e usando suas credenciais da Microsoft.
2. Selecione "**+ Create a resource**" ![image](https://github.com/r2WillDev/LAB-MachineLearning-Azure-ML/assets/106842143/bf711bd3-ca8f-430f-8c11-2ffe4f9f6c3b)
- Procure por _Azure AI services_ ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/45a49788-8f11-4a54-8aa6-b242fed0cd5e)
- Selecione criar um plano de serviços de IA do Azure. Você será levado a uma página para criar um recurso de serviços de **IA do Azure**. Configure-o com as seguintes configurações:
  - **Assinatura:** sua assinatura do Azure.
  - **Grupo de recursos:** selecione ou crie um grupo de recursos com um nome exclusivo.
  - **Região:** Leste dos EUA.
  - **Nome:** insira um nome exclusivo.
  - **Nível de preços:** Standard S0. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/c0febe11-0a48-465a-b6fd-57ce70ffaa36)

Ao marcar esta caixa, reconheço que li e entendi todos os termos abaixo: _Selecionado._

3. Selecione **Review + Create** e, em seguida, **Criate** e aguarde a conclusão da implantação.

## Conectar seu recurso de serviço de IA do Azure ao Vision Studio
Em seguida, conecte o recurso de serviço de IA do Azure provisionado acima ao Vision Studio.

1. Em outra guia do navegador, navegue até o [Vision Studio](https://portal.vision.cognitive.azure.com/gallery/featured).
2. Entre com sua conta e verifique se você está usando o mesmo diretório em que criou seu recurso de serviços de IA do Azure.
3. Na home page do Vision Studio, selecione **View all resources** no cabeçalho Introdução ao Vision. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/45f2d936-2584-48f1-8131-0758d6a22fbd)
4. Na página **Select a resource to work with**, passe o cursor do mouse sobre o recurso criado acima na lista e marque a caixa à esquerda do nome do recurso e selecione **Select as default resource**.

> [!NOTE]
> Se o recurso não estiver listado, talvez seja necessário atualizar a página.

![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/74fa0b2b-f169-4212-959e-2a73634c4ef8)

5. Feche a página de configurações selecionando o "x" no canto superior direito da tela.

## Detectar rostos no Vision Studio

1. Na página inicial **Get started with Vision**, selecione a guia **Face** e selecione o bloco **Detect faces in an image**. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/d09641c1-face-4112-a0b2-fba7ce26c1fa)
2. No subtítulo **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/03967add-9c18-4be4-a0fd-53454dfdd15d)
3. Selecione cada uma das imagens de amostra ou faça o upload de algum arquivo e observe os dados de detecção de rosto retornados. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/13241dd9-8f17-4237-9ce5-87294e9280da)

## Gerar legendas para uma imagem
Vejamos a funcionalidade de legendagem de imagem do Azure AI Vision. As legendas de imagem estão disponíveis por meio dos recursos **captions** e **dense caption**.

1. Na página inicial **Get started with Vision**, selecione a guia **Image analysis** e selecione o bloco **add captions to images**. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/34a42240-b62c-4a71-90cb-f37cc139d7de)
2. No subtítulo **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/19eee724-36b1-415e-86d3-86ddd33320ab)
3. Selecione cada uma das imagens de amostra ou faça upload de algum arquivo e observe os dados de detecção de rosto retornos.
4. Observe o texto da legenda gerado, visível no painel Atributos detectados à direita da imagem. A funcionalidade Legenda fornece uma única frase em inglês legível por humanos que descreve o conteúdo da imagem.![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/7d45a255-b8c7-4c07-b67d-4e19b14c28a6)

## Extrair texto de imagens no Vision Studio

1. Na página inicial **Get started with Vision**, selecione a guia **Optical character recognition** e selecione o bloco **Extract text from images**. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/0f4f2dbd-cbb2-4daa-8401-3fd5d955054b)
2. No subtítulo **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa. ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/d18ff0c6-9225-4473-8242-af8049fff150)
3. Selecione cada uma das imagens de amostra ou faça upload de algum arquivo e Agora reveja o que é devolvido:
   - Em Atributos detectados, qualquer texto encontrado na imagem é organizado em uma estrutura hierárquica de regiões, linhas e palavras.
   - Na imagem, a localização do texto é indicada por uma caixa delimitadora, como mostrado aqui: ![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/f79e5bf5-2691-4160-aae9-0b394848c4f2)]
  
# Apagar
Se você não pretende fazer mais exercícios, exclua todos os recursos que não são mais necessários. Isso evita o acúmulo de custos desnecessários.

1. Abra o [portal do Azure](https://portal.azure.com) e selecione o grupo de recursos que contém o recurso que você criou.![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/33d59956-1259-4ac4-9846-72d56f4daf75)

2. Selecione o recurso e selecione **Delete** e, em seguida, Sim para confirmar. O recurso é excluído.![image](https://github.com/r2WillDev/Reconhecimento-Facial-e-transformacao-de-imagens-em-Dados-no-Azure-ML/assets/106842143/76cbba71-d89f-45ad-b303-5085ad97c531)


> [!IMPORTANT]
> Todo esse passo a passo está no [site oficial da microsoft](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/05-ocr.html).















