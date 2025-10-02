<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T19:20:12+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "hu"
}
-->
# Kurzus Beállítása

## Bevezetés

Ebben a leckében megtanulhatod, hogyan futtasd a kurzus kódmintáit.

## Csatlakozz Más Tanulókhoz és Kérj Segítséget

Mielőtt elkezdenéd klónozni a repót, csatlakozz az [AI Agents For Beginners Discord csatornához](https://aka.ms/ai-agents/discord), hogy segítséget kapj a beállításhoz, kérdéseket tegyél fel a kurzussal kapcsolatban, vagy kapcsolatba lépj más tanulókkal.

## Klónozd vagy Forkold a Repót

Először klónozd vagy forkold a GitHub repót. Ezáltal létrehozod a kurzus anyagainak saját verzióját, amelyet futtathatsz, tesztelhetsz és módosíthatsz!

Ezt úgy teheted meg, hogy rákattintasz a <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">repo forkolása</a> linkre.

Most már rendelkezel a kurzus saját forkolt verziójával az alábbi linken:

![Forkolt Repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.hu.png)

## A Kód Futtatása

Ez a kurzus Jupyter Notebookokat kínál, amelyeket futtathatsz, hogy gyakorlati tapasztalatot szerezz az AI Agentek építésében.

A kódminták az alábbiakat használják:

**GitHub Fiók Szükséges - Ingyenes**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Jelölve mint (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace. Jelölve mint (autogen.ipynb)

**Azure Előfizetés Szükséges**:
3) Azure AI Foundry + Azure AI Agent Service. Jelölve mint (azureaiagent.ipynb)

Javasoljuk, hogy próbáld ki mindhárom példát, hogy megtudd, melyik működik a legjobban számodra.

Az általad választott opció határozza meg, hogy melyik beállítási lépéseket kell követned az alábbiakban:

## Követelmények

- Python 3.12+
  - **NOTE**: Ha nincs telepítve a Python 3.12, győződj meg róla, hogy telepíted. Ezután hozz létre egy venv-t python3.12 használatával, hogy biztosítsd a requirements.txt fájlban szereplő megfelelő verziók telepítését.
  
    >Példa

    Python venv könyvtár létrehozása:

    ``` bash
    python3 -m venv venv
    ```

    Ezután aktiváld a venv környezetet:

    macOS és Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- GitHub Fiók - A GitHub Models Marketplace eléréséhez
- Azure Előfizetés - Az Azure AI Foundry eléréséhez
- Azure AI Foundry Fiók - Az Azure AI Agent Service eléréséhez

A repó gyökérkönyvtárában található egy `requirements.txt` fájl, amely tartalmazza az összes szükséges Python csomagot a kódminták futtatásához.

Ezeket a következő parancs futtatásával telepítheted a terminálban, a repó gyökérkönyvtárában:

```bash
pip install -r requirements.txt
```
Javasoljuk, hogy hozz létre egy Python virtuális környezetet, hogy elkerüld az esetleges konfliktusokat és problémákat.

## VSCode Beállítása
Győződj meg róla, hogy a megfelelő Python verziót használod a VSCode-ban.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Beállítás GitHub Modellek Mintákhoz 

### 1. lépés: GitHub Személyes Hozzáférési Token (PAT) Lekérése

Ez a kurzus a GitHub Models Marketplace-t használja, amely ingyenes hozzáférést biztosít Nagy Nyelvi Modellekhez (LLM-ekhez), amelyeket az AI Agentek építéséhez fogsz használni.

A GitHub Modellek használatához létre kell hoznod egy [GitHub Személyes Hozzáférési Tokent](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Ezt úgy teheted meg, hogy ellátogatsz a <a href="https://github.com/settings/personal-access-tokens" target="_blank">Személyes Hozzáférési Tokenek beállításai</a> oldalra a GitHub fiókodban.

Kérjük, kövesd a [Legkisebb Jogosultság Elvét](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) a token létrehozásakor. Ez azt jelenti, hogy csak azokat a jogosultságokat add meg a tokennek, amelyek szükségesek a kurzus kódmintáinak futtatásához.

1. Válaszd ki a `Fine-grained tokens` opciót a képernyő bal oldalán, a **Fejlesztői beállítások** menüpont alatt.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.hu.png)

    Ezután válaszd a `Generate new token` lehetőséget.

    ![Token Generálása](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.hu.png)

2. Adj meg egy leíró nevet a tokennek, amely tükrözi annak célját, hogy később könnyen azonosítható legyen.


    🔐 Token Időtartam Ajánlás

    Ajánlott időtartam: 30 nap
    Biztonságosabb megoldásként választhatsz rövidebb időszakot is—például 7 nap 🛡️
    Ez egy remek módja annak, hogy személyes célt állíts be, és befejezd a kurzust, miközben a tanulási lendületed magas 🚀.

    ![Token Név és Lejárati Idő](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.hu.png)

3. Korlátozd a token hatókörét a repó forkjára.

    ![Hatókör Korlátozása Forkolt Repóra](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.hu.png)

4. Korlátozd a token jogosultságait: A **Permissions** alatt kattints az **Account** fülre, majd kattints a "+ Add permissions" gombra. Egy legördülő menü jelenik meg. Keresd meg a **Models** opciót, és jelöld be a négyzetet.
    ![Modellek Jogosultság Hozzáadása](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.hu.png)

5. Ellenőrizd a szükséges jogosultságokat a token generálása előtt. ![Jogosultságok Ellenőrzése](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.hu.png)

6. A token generálása előtt győződj meg róla, hogy készen állsz a token biztonságos tárolására, például egy jelszókezelőben, mivel a token nem lesz újra látható a létrehozás után. ![Token Biztonságos Tárolása](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.hu.png)

Másold ki az újonnan létrehozott tokent. Most add hozzá ezt a `.env` fájlhoz, amelyet a kurzus tartalmaz.


### 2. lépés: `.env` Fájl Létrehozása

A `.env` fájl létrehozásához futtasd az alábbi parancsot a terminálban.

```bash
cp .env.example .env
```

Ez lemásolja a példa fájlt, és létrehoz egy `.env` fájlt a könyvtáradban, ahol kitöltheted a környezeti változók értékeit.

A tokened másolása után nyisd meg a `.env` fájlt a kedvenc szövegszerkesztődben, és illeszd be a tokent a `GITHUB_TOKEN` mezőbe.
![GitHub Token Mező](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.hu.png)


Most már képesnek kell lenned futtatni a kurzus kódmintáit.

## Beállítás Azure AI Foundry és Azure AI Agent Service Mintákhoz

### 1. lépés: Azure Projekt Végpont Lekérése


Kövesd az Azure AI Foundry hub és projekt létrehozásának lépéseit itt: [Hub erőforrások áttekintése](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)


Miután létrehoztad a projektedet, le kell kérned a projekt kapcsolatának karakterláncát.

Ezt úgy teheted meg, hogy ellátogatsz a **Áttekintés** oldalra a projektedben az Azure AI Foundry portálon.

![Projekt Kapcsolat Karakterlánc](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.hu.png)

### 2. lépés: `.env` Fájl Létrehozása

A `.env` fájl létrehozásához futtasd az alábbi parancsot a terminálban.

```bash
cp .env.example .env
```

Ez lemásolja a példa fájlt, és létrehoz egy `.env` fájlt a könyvtáradban, ahol kitöltheted a környezeti változók értékeit.

A tokened másolása után nyisd meg a `.env` fájlt a kedvenc szövegszerkesztődben, és illeszd be a tokent a `PROJECT_ENDPOINT` mezőbe.

### 3. lépés: Bejelentkezés az Azure-ba

Biztonsági legjobb gyakorlatként [kulcs nélküli hitelesítést](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) fogunk használni az Azure OpenAI hitelesítéséhez a Microsoft Entra ID-val. 

Ezután nyiss meg egy terminált, és futtasd az `az login --use-device-code` parancsot, hogy bejelentkezz az Azure fiókodba.

Miután bejelentkeztél, válaszd ki az előfizetésedet a terminálban.


## További Környezeti Változók - Azure Search és Azure OpenAI 

Az Agentic RAG Leckéhez - 5. lecke - vannak minták, amelyek Azure Search és Azure OpenAI-t használnak.

Ha futtatni szeretnéd ezeket a mintákat, hozzá kell adnod az alábbi környezeti változókat a `.env` fájlodhoz:

### Áttekintés Oldal (Projekt)

- `AZURE_SUBSCRIPTION_ID` - Ellenőrizd a **Projekt részletek** részt a projekt **Áttekintés** oldalán.

- `AZURE_AI_PROJECT_NAME` - Nézd meg a projekt **Áttekintés** oldalának tetejét.

- `AZURE_OPENAI_SERVICE` - Ezt az **Azure OpenAI Service** **Tartalmazott képességek** fülén találod az **Áttekintés** oldalon.

### Menedzsment Központ

- `AZURE_OPENAI_RESOURCE_GROUP` - Menj a **Projekt tulajdonságok** részhez az **Áttekintés** oldalon a **Menedzsment Központban**.

- `GLOBAL_LLM_SERVICE` - Az **Kapcsolt erőforrások** alatt keresd meg az **Azure AI Services** kapcsolat nevét. Ha nem található, ellenőrizd az **Azure portált** az erőforráscsoportodban az AI Services erőforrás nevét.

### Modellek + Végpontok Oldal

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Válaszd ki az embedding modelledet (pl. `text-embedding-ada-002`), és jegyezd fel a **Deployment name**-et a modell részleteiből.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Válaszd ki a chat modelledet (pl. `gpt-4o-mini`), és jegyezd fel a **Deployment name**-et a modell részleteiből.

### Azure Portál

- `AZURE_OPENAI_ENDPOINT` - Keresd meg az **Azure AI services**-t, kattints rá, majd menj a **Erőforrás Menedzsment**, **Kulcsok és Végpont**, görgess le az "Azure OpenAI végpontok" részhez, és másold ki azt, amelyik "Nyelvi API-kat" mond.

- `AZURE_OPENAI_API_KEY` - Ugyanazon a képernyőn másold ki az 1. vagy 2. kulcsot.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Keresd meg az **Azure AI Search** erőforrásodat, kattints rá, és nézd meg az **Áttekintés** részt.

- `AZURE_SEARCH_API_KEY` - Ezután menj a **Beállítások** részhez, majd a **Kulcsok** részhez, hogy lemásold az elsődleges vagy másodlagos admin kulcsot.

### Külső Weboldal

- `AZURE_OPENAI_API_VERSION` - Látogasd meg az [API verzió életciklus](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) oldalt a **Legújabb GA API kiadás** alatt.

### Kulcs nélküli hitelesítés beállítása

Ahelyett, hogy a hitelesítő adatokat kódolnánk, kulcs nélküli kapcsolatot fogunk használni az Azure OpenAI-val. Ehhez importáljuk a `DefaultAzureCredential`-t, majd később meghívjuk a `DefaultAzureCredential` függvényt a hitelesítő adat megszerzéséhez.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Elakadtál Valahol?

Ha bármilyen problémád van a beállítás futtatásával, csatlakozz az <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI Közösség Discord</a>-hoz, vagy <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">hozz létre egy hibajelentést</a>.

## Következő Lecke

Most már készen állsz a kurzus kódjának futtatására. Jó tanulást az AI Agentek világáról! 

[Bevezetés az AI Agentekbe és az Agent Használati Esetekbe](../01-intro-to-ai-agents/README.md)

---

**Felelősségi nyilatkozat**:  
Ez a dokumentum az [Co-op Translator](https://github.com/Azure/co-op-translator) AI fordítási szolgáltatás segítségével került lefordításra. Bár törekszünk a pontosságra, kérjük, vegye figyelembe, hogy az automatikus fordítások hibákat vagy pontatlanságokat tartalmazhatnak. Az eredeti dokumentum az eredeti nyelvén tekintendő hiteles forrásnak. Kritikus információk esetén javasolt professzionális emberi fordítást igénybe venni. Nem vállalunk felelősséget semmilyen félreértésért vagy téves értelmezésért, amely a fordítás használatából eredhet.