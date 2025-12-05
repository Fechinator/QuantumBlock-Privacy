# Adding a New Language

## Android App Localization

1.  **Create a new resource directory**:
    - Go to `app/src/main/res/`.
    - Create a folder named `values-xx`, where `xx` is the ISO 639-1 language code (e.g., `values-fr` for French, `values-es` for Spanish).

2.  **Copy Strings**:
    - Copy `app/src/main/res/values/strings.xml` (the English default) into your new folder.

3.  **Translate**:
    - Open the new `strings.xml`.
    - Translate the text inside the `<string>` tags. **Do not change the `name` attributes.**

    ```xml
    <!-- Example for Spanish (values-es/strings.xml) -->
    <string name="app_name">QuantumBlock</string>
    <string name="nav_home">Inicio</string>
    ```

## Privacy Policy Website (`docs/index.html`)

1.  **Add Content**:
    - Open `docs/index.html`.
    - Copy the English content section `<div id="en-content" class="content">`.
    - Paste it and change the ID to the language code (e.g., `id="fr-content"`).
    - Translate the content inside.

2.  **Update JavaScript**:
    - Locate the `showLanguage` function script at the bottom of the file.
    - Add a new `else if` block for your language code:

    ```javascript
    } else if (userLang.startsWith('fr')) {
        document.getElementById('fr-content').style.display = 'block';
    }
    ```
