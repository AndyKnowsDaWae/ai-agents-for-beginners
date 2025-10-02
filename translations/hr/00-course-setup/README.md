<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T19:23:42+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "hr"
}
-->
# Postavljanje tečaja

## Uvod

Ova lekcija pokriva kako pokrenuti primjere koda iz ovog tečaja.

## Pridružite se drugim polaznicima i zatražite pomoć

Prije nego što počnete klonirati svoj repozitorij, pridružite se [Discord kanalu AI Agents For Beginners](https://aka.ms/ai-agents/discord) kako biste dobili pomoć oko postavljanja, postavili pitanja o tečaju ili se povezali s drugim polaznicima.

## Klonirajte ili forkajte ovaj repozitorij

Za početak, klonirajte ili forkajte GitHub repozitorij. Time ćete dobiti vlastitu verziju materijala tečaja kako biste mogli pokretati, testirati i prilagođavati kod!

To možete učiniti klikom na poveznicu za <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">forkanje repozitorija</a>.

Sada biste trebali imati vlastitu forkanu verziju ovog tečaja na sljedećoj poveznici:

![Forkani repozitorij](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.hr.png)

## Pokretanje koda

Ovaj tečaj nudi niz Jupyter Notebooks datoteka koje možete pokrenuti kako biste stekli praktično iskustvo u izradi AI agenata.

Primjeri koda koriste:

**Zahtijeva GitHub račun - Besplatno**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Označeno kao (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace. Označeno kao (autogen.ipynb)

**Zahtijeva Azure pretplatu**:
3) Azure AI Foundry + Azure AI Agent Service. Označeno kao (azureaiagent.ipynb)

Preporučujemo da isprobate sve tri vrste primjera kako biste vidjeli koji vam najbolje odgovara.

Ovisno o opciji koju odaberete, slijedite odgovarajuće korake za postavljanje u nastavku:

## Zahtjevi

- Python 3.12+
  - **NAPOMENA**: Ako nemate instaliran Python 3.12, osigurajte da ga instalirate. Zatim kreirajte svoj venv koristeći python3.12 kako biste osigurali da se instaliraju ispravne verzije iz datoteke requirements.txt.
  
    >Primjer

    Kreirajte direktorij za Python venv:

    ``` bash
    python3 -m venv venv
    ```

    Zatim aktivirajte venv okruženje za:

    macOS i Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- GitHub račun - Za pristup GitHub Models Marketplaceu
- Azure pretplata - Za pristup Azure AI Foundryju
- Azure AI Foundry račun - Za pristup Azure AI Agent Serviceu

U korijenu ovog repozitorija uključili smo datoteku `requirements.txt` koja sadrži sve potrebne Python pakete za pokretanje primjera koda.

Možete ih instalirati pokretanjem sljedeće naredbe u terminalu u korijenu repozitorija:

```bash
pip install -r requirements.txt
```
Preporučujemo kreiranje Python virtualnog okruženja kako biste izbjegli konflikte i probleme.

## Postavljanje VSCode-a
Provjerite koristite li ispravnu verziju Pythona u VSCode-u.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Postavljanje za primjere koji koriste GitHub modele 

### Korak 1: Dohvatite svoj GitHub Personal Access Token (PAT)

Ovaj tečaj koristi GitHub Models Marketplace, koji pruža besplatan pristup velikim jezičnim modelima (LLM-ovima) koje ćete koristiti za izradu AI agenata.

Za korištenje GitHub modela, trebate kreirati [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

To možete učiniti odlaskom na <a href="https://github.com/settings/personal-access-tokens" target="_blank">postavke za Personal Access Token</a> u svom GitHub računu.

Molimo slijedite [Princip najmanjih privilegija](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) prilikom kreiranja tokena. To znači da tokenu trebate dodijeliti samo one dozvole koje su potrebne za pokretanje primjera koda u ovom tečaju.

1. Odaberite opciju `Fine-grained tokens` na lijevoj strani ekrana tako da odete na **Developer settings**.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.hr.png)

    Zatim odaberite `Generate new token`.

    ![Generiraj token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.hr.png)

2. Unesite opisni naziv za svoj token koji odražava njegovu svrhu, kako biste ga kasnije lako identificirali.


    🔐 Preporuka za trajanje tokena

    Preporučeno trajanje: 30 dana  
    Za sigurniji pristup možete odabrati kraći period—na primjer, 7 dana 🛡️  
    To je odličan način da postavite osobni cilj i završite tečaj dok je vaš entuzijazam za učenje visok 🚀.

    ![Naziv i trajanje tokena](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.hr.png)

3. Ograničite opseg tokena na svoj fork ovog repozitorija.

    ![Ograničite opseg na fork repozitorij](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.hr.png)

4. Ograničite dozvole tokena: Pod **Permissions**, kliknite na karticu **Account** i pritisnite gumb "+ Add permissions". Pojavit će se padajući izbornik. Potražite **Models** i označite okvir za njega.
    ![Dodajte dozvolu za modele](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.hr.png)

5. Provjerite potrebne dozvole prije generiranja tokena. ![Provjerite dozvole](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.hr.png)

6. Prije generiranja tokena, osigurajte da ste spremni pohraniti token na sigurno mjesto, poput trezora za lozinke, jer se neće ponovno prikazati nakon što ga kreirate. ![Sigurno pohranite token](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.hr.png)

Kopirajte svoj novi token koji ste upravo kreirali. Sada ćete ga dodati u svoju `.env` datoteku uključenu u ovaj tečaj.


### Korak 2: Kreirajte svoju `.env` datoteku

Za kreiranje `.env` datoteke pokrenite sljedeću naredbu u terminalu.

```bash
cp .env.example .env
```

Ovo će kopirati primjer datoteke i kreirati `.env` u vašem direktoriju, gdje ćete popuniti vrijednosti za varijable okruženja.

S kopiranim tokenom, otvorite `.env` datoteku u svom omiljenom uređivaču teksta i zalijepite svoj token u polje `GITHUB_TOKEN`.
![Polje za GitHub token](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.hr.png)


Sada biste trebali moći pokrenuti primjere koda iz ovog tečaja.

## Postavljanje za primjere koji koriste Azure AI Foundry i Azure AI Agent Service

### Korak 1: Dohvatite svoj Azure projektni endpoint


Slijedite korake za kreiranje huba i projekta u Azure AI Foundryju ovdje: [Pregled resursa huba](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)


Nakon što ste kreirali svoj projekt, trebate dohvatiti vezni niz za svoj projekt.

To možete učiniti odlaskom na stranicu **Overview** svog projekta u Azure AI Foundry portalu.

![Vezni niz projekta](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.hr.png)

### Korak 2: Kreirajte svoju `.env` datoteku

Za kreiranje `.env` datoteke pokrenite sljedeću naredbu u terminalu.

```bash
cp .env.example .env
```

Ovo će kopirati primjer datoteke i kreirati `.env` u vašem direktoriju, gdje ćete popuniti vrijednosti za varijable okruženja.

S kopiranim tokenom, otvorite `.env` datoteku u svom omiljenom uređivaču teksta i zalijepite svoj token u polje `PROJECT_ENDPOINT`.

### Korak 3: Prijavite se na Azure

Kao sigurnosnu najbolju praksu, koristit ćemo [autentifikaciju bez ključa](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) za autentifikaciju na Azure OpenAI s Microsoft Entra ID-om. 

Zatim otvorite terminal i pokrenite `az login --use-device-code` kako biste se prijavili na svoj Azure račun.

Nakon što se prijavite, odaberite svoju pretplatu u terminalu.


## Dodatne varijable okruženja - Azure Search i Azure OpenAI 

Za lekciju Agentic RAG - Lekcija 5 - postoje primjeri koji koriste Azure Search i Azure OpenAI.

Ako želite pokrenuti ove primjere, trebate dodati sljedeće varijable okruženja u svoju `.env` datoteku:

### Stranica Pregled (Projekt)

- `AZURE_SUBSCRIPTION_ID` - Provjerite **Project details** na stranici **Overview** svog projekta.

- `AZURE_AI_PROJECT_NAME` - Pogledajte vrh stranice **Overview** za svoj projekt.

- `AZURE_OPENAI_SERVICE` - Pronađite ovo na kartici **Included capabilities** za **Azure OpenAI Service** na stranici **Overview**.

### Centar za upravljanje

- `AZURE_OPENAI_RESOURCE_GROUP` - Idite na **Project properties** na stranici **Overview** u **Management Centeru**.

- `GLOBAL_LLM_SERVICE` - Pod **Connected resources**, pronađite naziv veze za **Azure AI Services**. Ako nije navedeno, provjerite **Azure portal** pod svojom grupom resursa za naziv resursa AI Services.

### Stranica Modeli + Endpointi

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Odaberite svoj model za ugrađivanje (npr. `text-embedding-ada-002`) i zabilježite **Deployment name** iz detalja modela.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Odaberite svoj model za chat (npr. `gpt-4o-mini`) i zabilježite **Deployment name** iz detalja modela.

### Azure portal

- `AZURE_OPENAI_ENDPOINT` - Pronađite **Azure AI services**, kliknite na njega, zatim idite na **Resource Management**, **Keys and Endpoint**, pomaknite se dolje do "Azure OpenAI endpoints" i kopirajte onaj koji kaže "Language APIs".

- `AZURE_OPENAI_API_KEY` - Na istoj stranici, kopirajte KLJUČ 1 ili KLJUČ 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Pronađite svoj **Azure AI Search** resurs, kliknite na njega i pogledajte **Overview**.

- `AZURE_SEARCH_API_KEY` - Zatim idite na **Settings** i zatim **Keys** kako biste kopirali primarni ili sekundarni administratorski ključ.

### Vanjska web stranica

- `AZURE_OPENAI_API_VERSION` - Posjetite stranicu [API verzije](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) pod **Latest GA API release**.

### Postavljanje autentifikacije bez ključa

Umjesto da hardkodiramo vaše vjerodajnice, koristit ćemo vezu bez ključa s Azure OpenAI. Za to ćemo uvesti `DefaultAzureCredential` i kasnije pozvati funkciju `DefaultAzureCredential` za dobivanje vjerodajnice.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Imate li problema?

Ako imate bilo kakvih problema s ovim postavljanjem, pridružite se našem <a href="https://discord.gg/kzRShWzttr" target="_blank">Discordu Azure AI zajednice</a> ili <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">kreirajte problem</a>.

## Sljedeća lekcija

Sada ste spremni pokrenuti kod za ovaj tečaj. Sretno u učenju o svijetu AI agenata! 

[Uvod u AI agente i primjene agenata](../01-intro-to-ai-agents/README.md)

---

**Odricanje od odgovornosti**:  
Ovaj dokument je preveden pomoću AI usluge za prevođenje [Co-op Translator](https://github.com/Azure/co-op-translator). Iako nastojimo osigurati točnost, imajte na umu da automatski prijevodi mogu sadržavati pogreške ili netočnosti. Izvorni dokument na izvornom jeziku treba smatrati autoritativnim izvorom. Za ključne informacije preporučuje se profesionalni prijevod od strane čovjeka. Ne preuzimamo odgovornost za nesporazume ili pogrešna tumačenja koja mogu proizaći iz korištenja ovog prijevoda.