<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T17:10:25+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "fi"
}
-->
# Kurssin asennus

## Johdanto

Tässä osiossa käsitellään, miten kurssin koodiesimerkkejä suoritetaan.

## Liity muiden oppijoiden joukkoon ja pyydä apua

Ennen kuin alat kloonata reposi, liity [AI Agents For Beginners Discord-kanavalle](https://aka.ms/ai-agents/discord) saadaksesi apua asennukseen, kysymyksiin kurssista tai yhteyden muihin oppijoihin.

## Kloonaa tai haarauta tämä repo

Aloittaaksesi, kloonaa tai haarauta GitHub-repositorio. Tämä luo oman version kurssimateriaalista, jotta voit suorittaa, testata ja muokata koodia!

Tämä onnistuu napsauttamalla linkkiä <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">haaraamaan repo</a>.

Sinulla pitäisi nyt olla haarautettu versio tästä kurssista seuraavassa linkissä:

![Haarautettu repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.fi.png)

## Koodin suorittaminen

Tämä kurssi tarjoaa sarjan Jupyter Notebooks -tiedostoja, joita voit käyttää saadaksesi käytännön kokemusta AI-agenttien rakentamisesta.

Koodiesimerkit käyttävät joko:

**Vaatii GitHub-tilin - Ilmainen**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Merkitty nimellä (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace. Merkitty nimellä (autogen.ipynb)

**Vaatii Azure-tilauksen**:
3) Azure AI Foundry + Azure AI Agent Service. Merkitty nimellä (azureaiagent.ipynb)

Suosittelemme kokeilemaan kaikkia kolmea esimerkkiä nähdäksesi, mikä toimii parhaiten sinulle.

Valitsemasi vaihtoehto määrittää, mitkä asennusvaiheet sinun tulee suorittaa alla:

## Vaatimukset

- Python 3.12+
  - **NOTE**: Jos sinulla ei ole Python 3.12 asennettuna, varmista, että asennat sen. Luo sitten venv käyttämällä python3.12 varmistaaksesi, että oikeat versiot asennetaan requirements.txt-tiedostosta.
  
    >Esimerkki

    Luo Python venv-hakemisto:

    ``` bash
    python3 -m venv venv
    ```

    Aktivoi venv-ympäristö:

    macOS ja Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- GitHub-tili - Pääsy GitHub Models Marketplaceen
- Azure-tilaus - Pääsy Azure AI Foundryyn
- Azure AI Foundry -tili - Pääsy Azure AI Agent Serviceen

Olemme sisällyttäneet `requirements.txt`-tiedoston tämän repositorion juureen, joka sisältää kaikki tarvittavat Python-paketit koodiesimerkkien suorittamiseen.

Voit asentaa ne suorittamalla seuraavan komennon terminaalissa repositorion juuressa:

```bash
pip install -r requirements.txt
```
Suosittelemme Python-virtuaaliympäristön luomista välttääksesi konflikteja ja ongelmia.

## VSCode-asennus
Varmista, että käytät oikeaa Python-versiota VSCode:ssa.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Asennus GitHub Models -esimerkeille 

### Vaihe 1: Hanki GitHubin henkilökohtainen käyttöoikeustunnus (PAT)

Tämä kurssi hyödyntää GitHub Models Marketplacea, joka tarjoaa ilmaisen pääsyn suuriin kielimalleihin (LLM), joita käytät AI-agenttien rakentamiseen.

GitHub-mallien käyttämiseksi sinun tulee luoda [GitHubin henkilökohtainen käyttöoikeustunnus](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Tämä onnistuu siirtymällä <a href="https://github.com/settings/personal-access-tokens" target="_blank">henkilökohtaisten käyttöoikeustunnusten asetuksiin</a> GitHub-tililläsi.

Noudata [vähimmäisoikeuksien periaatetta](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) luodessasi tunnusta. Tämä tarkoittaa, että sinun tulisi antaa tunnukselle vain ne oikeudet, joita se tarvitsee kurssin koodiesimerkkien suorittamiseen.

1. Valitse `Fine-grained tokens` -vaihtoehto näytön vasemmasta reunasta siirtymällä **Developer settings** -osioon.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.fi.png)

    Valitse sitten `Generate new token`.

    ![Luo tunnus](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.fi.png)

2. Anna tunnukselle kuvaava nimi, joka heijastaa sen tarkoitusta, jotta se on helppo tunnistaa myöhemmin.


    🔐 Tunnuksen keston suositus

    Suositeltu kesto: 30 päivää  
    Turvallisemman käytännön vuoksi voit valita lyhyemmän ajan, kuten 7 päivää 🛡️  
    Tämä on hyvä tapa asettaa henkilökohtainen tavoite ja suorittaa kurssi, kun oppimisen vauhti on korkea 🚀.

    ![Tunnuksen nimi ja voimassaoloaika](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.fi.png)

3. Rajoita tunnuksen käyttöoikeudet haarautettuun repositorioon.

    ![Rajoita käyttöoikeudet haarautettuun repositorioon](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.fi.png)

4. Rajoita tunnuksen käyttöoikeudet: Valitse **Permissions**-kohdasta **Account**-välilehti ja napsauta "+ Add permissions" -painiketta. Näyttöön tulee pudotusvalikko. Etsi **Models** ja valitse sen ruutu.
    ![Lisää Models-käyttöoikeus](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.fi.png)

5. Varmista tarvittavat käyttöoikeudet ennen tunnuksen luomista. ![Varmista käyttöoikeudet](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.fi.png)

6. Ennen tunnuksen luomista varmista, että olet valmis tallentamaan tunnuksen turvalliseen paikkaan, kuten salasananhallintajärjestelmään, sillä sitä ei näytetä uudelleen luomisen jälkeen. ![Tallenna tunnus turvallisesti](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.fi.png)

Kopioi juuri luomasi tunnus. Lisää tämä kurssin mukana tulevaan `.env`-tiedostoon.


### Vaihe 2: Luo `.env`-tiedosto

Luo `.env`-tiedosto suorittamalla seuraava komento terminaalissa.

```bash
cp .env.example .env
```

Tämä kopioi esimerkkitiedoston ja luo `.env`-tiedoston hakemistoosi, jossa täytät ympäristömuuttujien arvot.

Kun tunnus on kopioitu, avaa `.env`-tiedosto suosikkitekstieditorissasi ja liitä tunnus `GITHUB_TOKEN`-kenttään.  
![GitHub Token -kenttä](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.fi.png)


Nyt sinun pitäisi pystyä suorittamaan kurssin koodiesimerkit.

## Asennus Azure AI Foundry- ja Azure AI Agent Service -esimerkeille

### Vaihe 1: Hanki Azure-projektin päätepiste


Seuraa ohjeita hubin ja projektin luomiseksi Azure AI Foundryssa täältä: [Hub-resurssien yleiskatsaus](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)


Kun olet luonut projektisi, sinun tulee hankkia projektin yhteysmerkkijono.

Tämä onnistuu siirtymällä projektisi **Overview**-sivulle Azure AI Foundry -portaalissa.

![Projektin yhteysmerkkijono](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.fi.png)

### Vaihe 2: Luo `.env`-tiedosto

Luo `.env`-tiedosto suorittamalla seuraava komento terminaalissa.

```bash
cp .env.example .env
```

Tämä kopioi esimerkkitiedoston ja luo `.env`-tiedoston hakemistoosi, jossa täytät ympäristömuuttujien arvot.

Kun tunnus on kopioitu, avaa `.env`-tiedosto suosikkitekstieditorissasi ja liitä tunnus `PROJECT_ENDPOINT`-kenttään.

### Vaihe 3: Kirjaudu Azureen

Turvallisuuskäytännön mukaisesti käytämme [avaimetonta autentikointia](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) Azure OpenAI:hin Microsoft Entra ID:n avulla. 

Avaa seuraavaksi terminaali ja suorita `az login --use-device-code` kirjautuaksesi Azure-tilillesi.

Kun olet kirjautunut sisään, valitse tilauksesi terminaalissa.


## Lisäympäristömuuttujat - Azure Search ja Azure OpenAI 

Agentic RAG -osiossa - osio 5 - on esimerkkejä, jotka käyttävät Azure Searchia ja Azure OpenAI:ta.

Jos haluat suorittaa nämä esimerkit, sinun tulee lisätä seuraavat ympäristömuuttujat `.env`-tiedostoosi:

### Yleiskatsaus-sivu (Projekti)

- `AZURE_SUBSCRIPTION_ID` - Tarkista **Project details** projektisi **Overview**-sivulta.

- `AZURE_AI_PROJECT_NAME` - Katso projektisi **Overview**-sivun yläosasta.

- `AZURE_OPENAI_SERVICE` - Löydät tämän **Included capabilities**-välilehdeltä **Azure OpenAI Service** kohdasta **Overview**-sivulla.

### Hallintakeskus

- `AZURE_OPENAI_RESOURCE_GROUP` - Siirry **Project properties** kohtaan **Overview**-sivulla **Management Centerissä**.

- `GLOBAL_LLM_SERVICE` - **Connected resources**-kohdassa löydät **Azure AI Services**-yhteyden nimen. Jos ei ole listattu, tarkista **Azure portal**-kohdasta resurssiryhmäsi AI Services -resurssin nimi.

### Models + Endpoints -sivu

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Valitse upotusmallisi (esim. `text-embedding-ada-002`) ja huomioi **Deployment name** mallin tiedoista.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Valitse chat-mallisi (esim. `gpt-4o-mini`) ja huomioi **Deployment name** mallin tiedoista.

### Azure-portaali

- `AZURE_OPENAI_ENDPOINT` - Etsi **Azure AI services**, napsauta sitä, siirry **Resource Management**, **Keys and Endpoint**, selaa alas kohtaan "Azure OpenAI endpoints" ja kopioi se, jossa lukee "Language APIs".

- `AZURE_OPENAI_API_KEY` - Kopioi samalta näytöltä KEY 1 tai KEY 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Etsi **Azure AI Search**-resurssi, napsauta sitä ja katso **Overview**.

- `AZURE_SEARCH_API_KEY` - Siirry **Settings** ja sitten **Keys** kopioidaksesi ensisijaisen tai toissijaisen hallintanäppäimen.

### Ulkoinen verkkosivu

- `AZURE_OPENAI_API_VERSION` - Käy [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) -sivulla kohdassa **Latest GA API release**.

### Avaimeton autentikointi

Sen sijaan, että kovakoodaisimme tunnistetiedot, käytämme avaimetonta yhteyttä Azure OpenAI:hin. Tätä varten tuomme `DefaultAzureCredential`-luokan ja kutsumme myöhemmin `DefaultAzureCredential`-funktiota saadaksemme tunnisteen.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Jäikö jokin epäselväksi?

Jos sinulla on ongelmia tämän asennuksen kanssa, liity <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI Community Discord</a>-kanavalle tai <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">luo ongelmaraportti</a>.

## Seuraava osio

Olet nyt valmis suorittamaan kurssin koodiesimerkit. Mukavaa oppimista AI-agenttien maailmasta! 

[Johdatus AI-agentteihin ja agenttien käyttötapauksiin](../01-intro-to-ai-agents/README.md)

---

**Vastuuvapauslauseke**:  
Tämä asiakirja on käännetty käyttämällä tekoälypohjaista käännöspalvelua [Co-op Translator](https://github.com/Azure/co-op-translator). Vaikka pyrimme tarkkuuteen, huomioithan, että automaattiset käännökset voivat sisältää virheitä tai epätarkkuuksia. Alkuperäinen asiakirja sen alkuperäisellä kielellä tulisi pitää ensisijaisena lähteenä. Kriittisen tiedon osalta suositellaan ammattimaista ihmiskäännöstä. Emme ole vastuussa väärinkäsityksistä tai virhetulkinnoista, jotka johtuvat tämän käännöksen käytöstä.