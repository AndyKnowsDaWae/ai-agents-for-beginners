<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T15:30:23+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "el"
}
-->
# Ρύθμιση Μαθήματος

## Εισαγωγή

Αυτό το μάθημα θα καλύψει πώς να εκτελέσετε τα δείγματα κώδικα αυτού του μαθήματος.

## Εγγραφείτε με άλλους μαθητές και λάβετε βοήθεια

Πριν ξεκινήσετε να κλωνοποιείτε το αποθετήριο σας, εγγραφείτε στο [κανάλι Discord AI Agents For Beginners](https://aka.ms/ai-agents/discord) για να λάβετε βοήθεια με τη ρύθμιση, να κάνετε ερωτήσεις σχετικά με το μάθημα ή να συνδεθείτε με άλλους μαθητές.

## Κλωνοποιήστε ή Δημιουργήστε Fork σε αυτό το Αποθετήριο

Για να ξεκινήσετε, παρακαλώ κλωνοποιήστε ή δημιουργήστε fork στο GitHub Repository. Αυτό θα δημιουργήσει τη δική σας έκδοση του υλικού του μαθήματος, ώστε να μπορείτε να εκτελέσετε, να δοκιμάσετε και να τροποποιήσετε τον κώδικα!

Αυτό μπορεί να γίνει κάνοντας κλικ στον σύνδεσμο για <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">δημιουργία fork στο αποθετήριο</a>.

Τώρα θα πρέπει να έχετε τη δική σας έκδοση του μαθήματος στον παρακάτω σύνδεσμο:

![Forked Repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.el.png)

## Εκτέλεση του Κώδικα

Αυτό το μάθημα προσφέρει μια σειρά από Jupyter Notebooks που μπορείτε να εκτελέσετε για να αποκτήσετε πρακτική εμπειρία στη δημιουργία AI Agents.

Τα δείγματα κώδικα χρησιμοποιούν είτε:

**Απαιτεί Λογαριασμό GitHub - Δωρεάν**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Ετικέτα: (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace. Ετικέτα: (autogen.ipynb)

**Απαιτεί Συνδρομή Azure**:
3) Azure AI Foundry + Azure AI Agent Service. Ετικέτα: (azureaiagent.ipynb)

Σας ενθαρρύνουμε να δοκιμάσετε και τους τρεις τύπους παραδειγμάτων για να δείτε ποιος σας ταιριάζει καλύτερα.

Η επιλογή που θα κάνετε θα καθορίσει ποια βήματα ρύθμισης πρέπει να ακολουθήσετε παρακάτω:

## Απαιτήσεις

- Python 3.12+
  - **ΣΗΜΕΙΩΣΗ**: Εάν δεν έχετε εγκατεστημένο το Python 3.12, βεβαιωθείτε ότι το εγκαταστήσατε. Στη συνέχεια, δημιουργήστε το venv χρησιμοποιώντας το python3.12 για να διασφαλίσετε ότι οι σωστές εκδόσεις εγκαθίστανται από το αρχείο requirements.txt.
  
    >Παράδειγμα

    Δημιουργία καταλόγου Python venv:

    ``` bash
    python3 -m venv venv
    ```

    Στη συνέχεια, ενεργοποιήστε το περιβάλλον venv για:

    macOS και Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- Λογαριασμός GitHub - Για πρόσβαση στο GitHub Models Marketplace
- Συνδρομή Azure - Για πρόσβαση στο Azure AI Foundry
- Λογαριασμός Azure AI Foundry - Για πρόσβαση στο Azure AI Agent Service

Έχουμε συμπεριλάβει ένα αρχείο `requirements.txt` στη ρίζα αυτού του αποθετηρίου που περιέχει όλα τα απαραίτητα πακέτα Python για την εκτέλεση των δειγμάτων κώδικα.

Μπορείτε να τα εγκαταστήσετε εκτελώντας την παρακάτω εντολή στο τερματικό σας στη ρίζα του αποθετηρίου:

```bash
pip install -r requirements.txt
```
Συνιστούμε τη δημιουργία ενός εικονικού περιβάλλοντος Python για να αποφύγετε τυχόν συγκρούσεις και προβλήματα.

## Ρύθμιση VSCode
Βεβαιωθείτε ότι χρησιμοποιείτε τη σωστή έκδοση του Python στο VSCode.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Ρύθμιση για Δείγματα με Χρήση GitHub Models 

### Βήμα 1: Αποκτήστε το Προσωπικό Access Token (PAT) του GitHub

Αυτό το μάθημα χρησιμοποιεί το GitHub Models Marketplace, παρέχοντας δωρεάν πρόσβαση σε Large Language Models (LLMs) που θα χρησιμοποιήσετε για να δημιουργήσετε AI Agents.

Για να χρησιμοποιήσετε τα GitHub Models, θα χρειαστεί να δημιουργήσετε ένα [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Αυτό μπορεί να γίνει πηγαίνοντας στις <a href="https://github.com/settings/personal-access-tokens" target="_blank">ρυθμίσεις Προσωπικών Access Tokens</a> στον λογαριασμό σας στο GitHub.

Παρακαλώ ακολουθήστε την [Αρχή της Ελάχιστης Απαραίτητης Πρόσβασης](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) κατά τη δημιουργία του token. Αυτό σημαίνει ότι πρέπει να δώσετε στο token μόνο τις άδειες που χρειάζεται για να εκτελέσει τα δείγματα κώδικα αυτού του μαθήματος.

1. Επιλέξτε την επιλογή `Fine-grained tokens` στην αριστερή πλευρά της οθόνης σας πηγαίνοντας στις **Ρυθμίσεις Προγραμματιστή**.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.el.png)

    Στη συνέχεια, επιλέξτε `Generate new token`.

    ![Generate Token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.el.png)

2. Εισάγετε ένα περιγραφικό όνομα για το token που αντικατοπτρίζει τον σκοπό του, ώστε να είναι εύκολο να το αναγνωρίσετε αργότερα.

    🔐 Σύσταση Διάρκειας Token

    Συνιστώμενη διάρκεια: 30 ημέρες
    Για πιο ασφαλή προσέγγιση, μπορείτε να επιλέξετε μικρότερη περίοδο—όπως 7 ημέρες 🛡️
    Είναι ένας εξαιρετικός τρόπος να θέσετε έναν προσωπικό στόχο και να ολοκληρώσετε το μάθημα ενώ η μαθησιακή σας ορμή είναι υψηλή 🚀.

    ![Token Name and Expiration](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.el.png)

3. Περιορίστε το πεδίο του token στο fork αυτού του αποθετηρίου.

    ![Limit scope to fork repository](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.el.png)

4. Περιορίστε τις άδειες του token: Στην καρτέλα **Permissions**, κάντε κλικ στην καρτέλα **Account** και πατήστε το κουμπί "+ Add permissions". Θα εμφανιστεί ένα dropdown. Αναζητήστε **Models** και επιλέξτε το κουτάκι.
    ![Add Models Permission](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.el.png)

5. Επαληθεύστε τις απαιτούμενες άδειες πριν δημιουργήσετε το token. ![Verify Permissions](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.el.png)

6. Πριν δημιουργήσετε το token, βεβαιωθείτε ότι είστε έτοιμοι να αποθηκεύσετε το token σε ασφαλές μέρος, όπως ένα θησαυροφυλάκιο διαχειριστή κωδικών πρόσβασης, καθώς δεν θα εμφανιστεί ξανά μετά τη δημιουργία του. ![Store Token Securely](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.el.png)

Αντιγράψτε το νέο token που μόλις δημιουργήσατε. Τώρα θα το προσθέσετε στο αρχείο `.env` που περιλαμβάνεται σε αυτό το μάθημα.

### Βήμα 2: Δημιουργήστε το Αρχείο `.env`

Για να δημιουργήσετε το αρχείο `.env`, εκτελέστε την παρακάτω εντολή στο τερματικό σας.

```bash
cp .env.example .env
```

Αυτό θα αντιγράψει το αρχείο παραδείγματος και θα δημιουργήσει ένα `.env` στον κατάλογό σας, όπου θα συμπληρώσετε τις τιμές για τις μεταβλητές περιβάλλοντος.

Με το token σας αντιγραμμένο, ανοίξτε το αρχείο `.env` στον αγαπημένο σας επεξεργαστή κειμένου και επικολλήστε το token στο πεδίο `GITHUB_TOKEN`.
![GitHub Token Field](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.el.png)

Τώρα θα πρέπει να μπορείτε να εκτελέσετε τα δείγματα κώδικα αυτού του μαθήματος.

## Ρύθμιση για Δείγματα με Χρήση Azure AI Foundry και Azure AI Agent Service

### Βήμα 1: Αποκτήστε το Endpoint του Έργου σας στο Azure

Ακολουθήστε τα βήματα για τη δημιουργία ενός hub και ενός έργου στο Azure AI Foundry που βρίσκονται εδώ: [Επισκόπηση πόρων Hub](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

Αφού δημιουργήσετε το έργο σας, θα χρειαστεί να αποκτήσετε τη συμβολοσειρά σύνδεσης για το έργο σας.

Αυτό μπορεί να γίνει πηγαίνοντας στη σελίδα **Επισκόπηση** του έργου σας στην πύλη Azure AI Foundry.

![Project Connection String](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.el.png)

### Βήμα 2: Δημιουργήστε το Αρχείο `.env`

Για να δημιουργήσετε το αρχείο `.env`, εκτελέστε την παρακάτω εντολή στο τερματικό σας.

```bash
cp .env.example .env
```

Αυτό θα αντιγράψει το αρχείο παραδείγματος και θα δημιουργήσει ένα `.env` στον κατάλογό σας, όπου θα συμπληρώσετε τις τιμές για τις μεταβλητές περιβάλλοντος.

Με το token σας αντιγραμμένο, ανοίξτε το αρχείο `.env` στον αγαπημένο σας επεξεργαστή κειμένου και επικολλήστε το token στο πεδίο `PROJECT_ENDPOINT`.

### Βήμα 3: Συνδεθείτε στο Azure

Ως βέλτιστη πρακτική ασφαλείας, θα χρησιμοποιήσουμε [keyless authentication](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) για να συνδεθούμε στο Azure OpenAI με το Microsoft Entra ID.

Στη συνέχεια, ανοίξτε ένα τερματικό και εκτελέστε `az login --use-device-code` για να συνδεθείτε στον λογαριασμό σας στο Azure.

Αφού συνδεθείτε, επιλέξτε τη συνδρομή σας στο τερματικό.

## Πρόσθετες Μεταβλητές Περιβάλλοντος - Azure Search και Azure OpenAI 

Για το μάθημα Agentic RAG - Μάθημα 5 - υπάρχουν δείγματα που χρησιμοποιούν Azure Search και Azure OpenAI.

Εάν θέλετε να εκτελέσετε αυτά τα δείγματα, θα χρειαστεί να προσθέσετε τις παρακάτω μεταβλητές περιβάλλοντος στο αρχείο `.env` σας:

### Σελίδα Επισκόπησης (Έργο)

- `AZURE_SUBSCRIPTION_ID` - Ελέγξτε τις **Λεπτομέρειες Έργου** στη σελίδα **Επισκόπηση** του έργου σας.

- `AZURE_AI_PROJECT_NAME` - Δείτε την κορυφή της σελίδας **Επισκόπηση** για το έργο σας.

- `AZURE_OPENAI_SERVICE` - Βρείτε αυτό στην καρτέλα **Included capabilities** για την **Υπηρεσία Azure OpenAI** στη σελίδα **Επισκόπηση**.

### Κέντρο Διαχείρισης

- `AZURE_OPENAI_RESOURCE_GROUP` - Μεταβείτε στις **Ιδιότητες Έργου** στη σελίδα **Επισκόπηση** του **Κέντρου Διαχείρισης**.

- `GLOBAL_LLM_SERVICE` - Στην ενότητα **Connected resources**, βρείτε το όνομα σύνδεσης **Azure AI Services**. Εάν δεν αναφέρεται, ελέγξτε την **πύλη Azure** στην ομάδα πόρων σας για το όνομα του πόρου AI Services.

### Σελίδα Μοντέλα + Endpoints

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Επιλέξτε το μοντέλο ενσωμάτωσης σας (π.χ., `text-embedding-ada-002`) και σημειώστε το **Deployment name** από τις λεπτομέρειες του μοντέλου.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Επιλέξτε το μοντέλο συνομιλίας σας (π.χ., `gpt-4o-mini`) και σημειώστε το **Deployment name** από τις λεπτομέρειες του μοντέλου.

### Πύλη Azure

- `AZURE_OPENAI_ENDPOINT` - Αναζητήστε τις **Υπηρεσίες Azure AI**, κάντε κλικ σε αυτές, στη συνέχεια μεταβείτε στη **Διαχείριση Πόρων**, **Κλειδιά και Endpoint**, και αντιγράψτε το endpoint που λέει "Language APIs".

- `AZURE_OPENAI_API_KEY` - Από την ίδια οθόνη, αντιγράψτε το ΚΛΕΙΔΙ 1 ή ΚΛΕΙΔΙ 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Βρείτε τον πόρο σας **Azure AI Search**, κάντε κλικ σε αυτόν και δείτε την **Επισκόπηση**.

- `AZURE_SEARCH_API_KEY` - Στη συνέχεια, μεταβείτε στις **Ρυθμίσεις** και μετά στα **Κλειδιά** για να αντιγράψετε το κύριο ή δευτερεύον κλειδί διαχειριστή.

### Εξωτερική Ιστοσελίδα

- `AZURE_OPENAI_API_VERSION` - Επισκεφθείτε τη σελίδα [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) στην ενότητα **Latest GA API release**.

### Ρύθμιση keyless authentication

Αντί να σκληροκωδικοποιήσουμε τα διαπιστευτήρια σας, θα χρησιμοποιήσουμε μια σύνδεση χωρίς κλειδιά με το Azure OpenAI. Για να το κάνουμε αυτό, θα εισάγουμε το `DefaultAzureCredential` και αργότερα θα καλέσουμε τη συνάρτηση `DefaultAzureCredential` για να λάβουμε το διαπιστευτήριο.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Κολλήσατε Κάπου;

Εάν αντιμετωπίζετε οποιοδήποτε πρόβλημα με αυτή τη ρύθμιση, μπείτε στο <a href="https://discord.gg/kzRShWzttr" target="_blank">Azure AI Community Discord</a> ή <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">δημιουργήστε ένα ζήτημα</a>.

## Επόμενο Μάθημα

Τώρα είστε έτοιμοι να εκτελέσετε τον κώδικα αυτού του μαθήματος. Καλή μάθηση για τον κόσμο των AI Agents! 

[Εισαγωγή στους AI Agents και Χρήσεις](../01-intro-to-ai-agents/README.md)

---

**Αποποίηση ευθύνης**:  
Αυτό το έγγραφο έχει μεταφραστεί χρησιμοποιώντας την υπηρεσία αυτόματης μετάφρασης [Co-op Translator](https://github.com/Azure/co-op-translator). Παρόλο που καταβάλλουμε προσπάθειες για ακρίβεια, παρακαλούμε να έχετε υπόψη ότι οι αυτοματοποιημένες μεταφράσεις ενδέχεται να περιέχουν λάθη ή ανακρίβειες. Το πρωτότυπο έγγραφο στη μητρική του γλώσσα θα πρέπει να θεωρείται η αυθεντική πηγή. Για κρίσιμες πληροφορίες, συνιστάται επαγγελματική ανθρώπινη μετάφραση. Δεν φέρουμε ευθύνη για τυχόν παρεξηγήσεις ή εσφαλμένες ερμηνείες που προκύπτουν από τη χρήση αυτής της μετάφρασης.