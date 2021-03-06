---

copyright:
  years: 2016
lastupdated: "2016-11-29"

---


<!-- Common attributes used in the template are defined as follows: -->
{:new_window: target="\_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}

# Configurando conectividade móvel e segurança
{: #iot4e_configureMCA}

Ative comunicações móveis e segurança configurando {{site.data.keyword.amafull}}. Essa tarefa é necessária para usar o aplicativo móvel de amostra e só precisa ser executada uma vez.
{:shortdesc}

Antes de iniciar, deve-se implementar uma instância do iniciador do {{site.data.keyword.iotelectronics}} na sua organização do {{site.data.keyword.Bluemix_notm}}. Implementar uma instância do iniciador
automaticamente implementa os aplicativos e serviços de componente, incluindo {{site.data.keyword.amafull}}.

1. Se você acabou de implementar o iniciador do {{site.data.keyword.iotelectronics}}, a guia Introdução do aplicativo iniciador será exibida e você deverá continuar para a próxima etapa
dessas instruções. Se o app iniciador não for exibido, abra seu painel do {{site.data.keyword.Bluemix_notm}} e inicie seu aplicativo iniciador do {{site.data.keyword.iotelectronics}} clicando no nome do aplicativo iniciador.

    ![{{site.data.keyword.iotelectronics}} no painel](images/IoT4E_bm_dashboard.svg "{{site.data.keyword.iotelectronics}} no painel")

2. Copie a URL do app da web do {{site.data.keyword.iotelectronics}} clicando com o botão direito em **Visualizar app** e selecionando **Copiar local de link**.

3. Na guia **Conexões**, clique no serviço do {{site.data.keyword.amashort}} para abri-lo.

3. Na página Autenticação do {{site.data.keyword.amashort}}, ative a autenticação clicando em **Ativar**.

4. Na seção **Customizado**, insira as credenciais de autenticação a seguir:

    - **Nome da região**: `myRealm`

    - **URL do provedor de identidade customizado**: cole a URL do aplicativo da API que você copiou na primeira etapa no formato a seguir: **https://<*myIoT4eStarterApp*>.mybluemix.net**.  

    **Importante:** assegure-se de que a URL use o protocolo seguro `https` mesmo que o valor copiado use `http`.

    - **URIs de redirecionamento de seu aplicativo da web**: deixe esse campo em branco.

   ![Configurar o {{site.data.keyword.amashort}}.](images/MCA_config_pg.svg "Página de autenticação do {{site.data.keyword.amashort}}")  

5. Salve suas configurações. Agora é possível retornar para o console de serviço do {{site.data.keyword.iotelectronics}} ou seu console do {{site.data.keyword.Bluemix_notm}}.
