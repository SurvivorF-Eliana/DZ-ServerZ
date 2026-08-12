# DayZ Clients Connect Hub - Multilingual README

---

## 🇪🇸 Español

# DayZ Clients Connect Hub
Panel táctico en un solo archivo HTML para centralizar las conexiones a los servidores de clientes en DayZ. Diseñado para ejecutarse 100% del lado del cliente, sin necesidad de backend, y conectarse directamente al juego con un clic.

### Características
* **Single-file HTML:** CSS y JS integrados. No requiere frameworks, dependencias ni builds. Se ejecuta abriendo el archivo en cualquier navegador.
* **Datos en tiempo real (DZSA API):** Consulta el estado de los servidores (nombre, mapa, jugadores online, cantidad de mods) conectando con la API de DZSA Launcher. Utiliza un proxy público (AllOrigins) para evitar bloqueos por CORS.
* **Cálculo de Query Port:** Solo se configura el puerto de juego (ej. `2302`). El script calcula y utiliza automáticamente el Query Port sumando `+1` (ej. `2303`) para las peticiones a la API.
* **Conexión Directa Steam:** Ejecuta el protocolo `steam://run/221100//-connect=IP -port=PUERTO`. Esto fuerza a Steam a lanzar el AppID de DayZ y le pasa los parámetros de conexión, permitiendo que el launcher oficial procese la descarga de mods necesarios. Manejado vía `window.location.href` para no cerrar la pestaña activa.

### Uso y Configuración
1. Descargar el archivo `.html`.
2. Abrir el archivo con cualquier editor de texto/código.
3. Buscar la sección `<div class="clients-grid">`.
4. Copiar y pegar el bloque de cualquier `.panel` que representa a un servidor para agregar uno nuevo.
5. Editar los parámetros `data-ip` y `data-game-port` en el HTML de la tarjeta:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Guardar los cambios. El panel actualizará la información visual automáticamente al abrirse.

### Notas Técnicas
* **Proxy de terceros:** La consulta a `dayzsalauncher.com/api/v1/query/` requiere pasar por `api.allorigins.win`. Si hay demoras en la carga de datos del servidor, suele ser por latencia de este servicio gratuito de puente.
* **Estilo Visual:** UI oscura (Dark/Lime) utilizando la tipografía *Host Grotesk* (importada vía Google Fonts). Diseño asimétrico de bordes orientado a herramientas client-side.

---

## 🇬🇧 English

# DayZ Clients Connect Hub
Tactical single-file HTML panel to centralize client server connections in DayZ. Designed to run 100% client-side, with no backend required, connecting directly to the game with one click.

### Features
* **Single-file HTML:** CSS and JS embedded. No frameworks, dependencies, or builds required. Runs by opening the file in any browser.
* **Real-time data (DZSA API):** Queries server status (name, map, online players, mod count) connecting to the DZSA Launcher API. Uses a public proxy (AllOrigins) to bypass CORS blocks.
* **Query Port Calculation:** Only the game port is configured (e.g., `2302`). The script automatically calculates and uses the Query Port by adding `+1` (e.g., `2303`) for API requests.
* **Steam Direct Connection:** Executes the protocol `steam://run/221100//-connect=IP -port=PORT`. This forces Steam to launch the DayZ AppID and passes the connection parameters, allowing the official launcher to process required mod downloads. Handled via `window.location.href` to prevent closing the active tab.

### Usage and Configuration
1. Download the `.html` file.
2. Open the file with any text/code editor.
3. Search for the `<div class="clients-grid">` section.
4. Copy and paste the block of any `.panel` representing a server to add a new one.
5. Edit the `data-ip` and `data-game-port` parameters in the card's HTML:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Save changes. The panel will automatically update visual information upon opening.

### Technical Notes
* **Third-party Proxy:** The query to `dayzsalauncher.com/api/v1/query/` requires passing through `api.allorigins.win`. Delays in loading server data are usually due to latency from this free bridge service.
* **Visual Style:** Dark/Lime UI using the *Host Grotesk* typography (imported via Google Fonts). Asymmetric border design geared towards client-side tools.

---

## 🇫🇷 Français

# Hub de Connexion Clients DayZ
Panneau tactique dans un seul fichier HTML pour centraliser les connexions aux serveurs des clients dans DayZ. Conçu pour s'exécuter 100% côté client, sans aucun backend nécessaire, permettant de se connecter directement au jeu en un clic.

### Fonctionnalités
* **HTML fichier unique :** CSS et JS intégrés. Aucun framework, dépendance ou build requis. S'exécute en ouvrant le fichier dans n'importe quel navigateur.
* **Données en temps réel (API DZSA) :** Interroge l'état des serveurs (nom, carte, joueurs en ligne, nombre de mods) via l'API de DZSA Launcher. Utilise un proxy public (AllOrigins) pour contourner les blocages CORS.
* **Calcul du port de requête (Query Port) :** Seul le port de jeu est configuré (ex: `2302`). Le script calcule et utilise automatiquement le Query Port en ajoutant `+1` (ex: `2303`) pour les requêtes API.
* **Connexion Directe Steam :** Exécute le protocole `steam://run/221100//-connect=IP -port=PORT`. Cela force Steam à lancer l'AppID de DayZ avec les paramètres de connexion, permettant au launcher officiel de télécharger les mods requis. Géré via `window.location.href` pour ne pas fermer l'onglet actif.

### Utilisation et Configuration
1. Téléchargez le fichier `.html`.
2. Ouvrez le fichier avec un éditeur de texte/code.
3. Cherchez la section `<div class="clients-grid">`.
4. Copiez et collez le bloc d'un `.panel` représentant un serveur pour en ajouter un nouveau.
5. Modifiez les paramètres `data-ip` et `data-game-port` dans le code HTML de la carte :
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Enregistrez les modifications. Le panneau mettra à jour les informations visuelles à l'ouverture.

### Notes Techniques
* **Proxy Tiers :** La requête vers `dayzsalauncher.com/api/v1/query/` passe par `api.allorigins.win`. Les éventuels retards de chargement sont souvent dus à la latence de ce service relais gratuit.
* **Style Visuel :** Interface Dark/Lime utilisant la police *Host Grotesk*. Design asymétrique adapté aux outils client-side.

---

## 🇮🇹 Italiano

# Hub di Connessione Client DayZ
Pannello tattico in un singolo file HTML per centralizzare le connessioni ai server dei client in DayZ. Progettato per essere eseguito 100% lato client, senza backend, collegandosi direttamente al gioco con un clic.

### Caratteristiche
* **HTML a file singolo:** CSS e JS integrati. Nessun framework, dipendenza o build necessaria. Si esegue aprendo il file in qualsiasi browser.
* **Dati in tempo reale (API DZSA):** Interroga lo stato dei server (nome, mappa, giocatori online, numero di mod) tramite l'API di DZSA Launcher. Utilizza un proxy pubblico (AllOrigins) per bypassare i blocchi CORS.
* **Calcolo del Query Port:** Viene configurato solo il port di gioco (es. `2302`). Lo script calcola automaticamente il Query Port aggiungendo `+1` (es. `2303`) per le richieste API.
* **Connessione Diretta Steam:** Esegue il protocollo `steam://run/221100//-connect=IP -port=PORT`. Questo forza Steam ad avviare l'AppID di DayZ e passa i parametri di connessione per scaricare le mod richieste dal launcher ufficiale. Gestito tramite `window.location.href` per non chiudere la scheda attiva.

### Utilizzo e Configurazione
1. Scarica il file `.html`.
2. Apri il file con un editor di testo/codice.
3. Cerca la sezione `<div class="clients-grid">`.
4. Copia e incolla il blocco di un `.panel` relativo a un server per aggiungerne uno nuovo.
5. Modifica i parametri `data-ip` e `data-game-port` nell'HTML della scheda:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Salva le modifiche. Il pannello si aggiornerà automaticamente all'apertura.

### Note Tecniche
* **Proxy di terze parti:** La query a `dayzsalauncher.com/api/v1/query/` passa da `api.allorigins.win`. Eventuali ritardi sono solitamente dovuti alla latenza di questo servizio gratuito.
* **Stile Visivo:** Interfaccia Dark/Lime con font *Host Grotesk*. Design asimmetrico orientato agli strumenti client-side.

---

## 🇩🇪 Deutsch

# DayZ Clients Connect Hub
Taktisches Single-File-HTML-Panel zur Zentralisierung von Client-Server-Verbindungen in DayZ. Läuft 100% clientseitig ohne Backend und verbindet mit einem Klick direkt ins Spiel.

### Eigenschaften
* **Single-File-HTML:** CSS und JS sind integriert. Keine Frameworks, Abhängigkeiten oder Builds erforderlich. Einfach im Browser öffnen.
* **Echtzeitdaten (DZSA API):** Fragt den Serverstatus (Name, Karte, Spieler online, Mod-Anzahl) über die DZSA Launcher API ab. Nutzt einen öffentlichen Proxy (AllOrigins) zur Umgehung von CORS-Blockaden.
* **Query-Port-Berechnung:** Nur der Game-Port wird konfiguriert (z.B. `2302`). Das Skript berechnet automatisch den Query-Port durch Addition von `+1` (z.B. `2303`) für API-Anfragen.
* **Steam Direct Connection:** Führt das Protokoll `steam://run/221100//-connect=IP -port=PORT` aus. Dies zwingt Steam, die DayZ-AppID mit den Verbindungsparametern zu starten, sodass der offizielle Launcher erforderliche Mods herunterladen kann. Umsetzung via `window.location.href`, um das Schließen des Tabs zu verhindern.

### Nutzung und Konfiguration
1. Die `.html`-Datei herunterladen.
2. Die Datei mit einem Text-/Code-Editor öffnen.
3. Den Abschnitt `<div class="clients-grid">` suchen.
4. Den Block eines `.panel` kopieren und einfügen, um einen neuen Server hinzuzufügen.
5. Die Parameter `data-ip` und `data-game-port` im HTML bearbeiten:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Speichern. Das Panel aktualisiert die Anzeige automatisch beim Öffnen.

### Technische Hinweise
* **Drittanbieter-Proxy:** Die Anfrage an `dayzsalauncher.com/api/v1/query/` läuft über `api.allorigins.win`. Ladeverzögerungen sind meist auf die Latenz dieses kostenlosen Dienstes zurückzuführen.
* **Visueller Stil:** Dark/Lime UI mit *Host Grotesk* Schriftart. Asymmetrisches Design für clientseitige Tools.

---

## 🇨🇿 Čeština

# DayZ Clients Connect Hub
Taktický HTML panel v jednom souboru pro centralizaci připojení ke klientským serverům v DayZ. Běží 100% na straně klienta, bez nutnosti backendu, s přímým připojením do hry na jedno kliknutí.

### Vlastnosti
* **HTML v jednom souboru:** CSS a JS jsou součástí souboru. Nejsou potřeba žádné frameworky ani závislosti. Stačí otevřít v prohlížeči.
* **Data v reálném čase (DZSA API):** Získává stav serveru (název, mapa, online hráči, počet modů) z DZSA Launcher API. K obcházení CORS blokací využívá veřejnou proxy (AllOrigins).
* **Výpočet Query Portu:** Konfiguruje se pouze herní port (např. `2302`). Skript automaticky vypočítá Query Port přidáním `+1` (např. `2303`) pro požadavky API.
* **Přímé připojení přes Steam:** Spouští protokol `steam://run/221100//-connect=IP -port=PORT`. To přinutí Steam spustit DayZ AppID a předat parametry připojení, což umožní oficiálnímu launcheru stáhnout potřebné mody. Řešeno přes `window.location.href`, aby se nezavřela aktivní karta.

### Použití a konfigurace
1. Stáhněte soubor `.html`.
2. Otevřete jej v textovém/kódovém editoru.
3. Najděte sekci `<div class="clients-grid">`.
4. Zkopírujte a vložte blok `.panel` pro přidání nového serveru.
5. Upravte parametry `data-ip` a `data-game-port` v HTML kartě:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Uložte změny. Panel se při otevření automaticky aktualizuje.

### Technické poznámky
* **Proxy třetích stran:** Dotazy na `dayzsalauncher.com/api/v1/query/` procházejí přes `api.allorigins.win`. Zpoždění v načítání dat je obvykle způsobeno latencí této bezplatné služby.
* **Vizuální styl:** Dark/Lime UI s písmem *Host Grotesk*. Asymetrický design pro client-side nástroje.

---

## 🇵🇱 Polski

# Hub Połączeń Klientów DayZ
Taktyczny panel w jednym pliku HTML do centralizacji połączeń z serwerami klientów w DayZ. Działa w 100% po stronie klienta, bez backendu, łącząc bezpośrednio z grą za pomocą jednego kliknięcia.

### Funkcje
* **Pojedynczy plik HTML:** CSS i JS zintegrowane w jednym pliku. Bez frameworków i zależności. Działa po otwarciu w przeglądarce.
* **Dane w czasie rzeczywistym (API DZSA):** Pobiera status serwera (nazwa, mapa, gracze online, liczba modów) z API DZSA Launcher. Używa publicznego proxy (AllOrigins) do obejścia blokad CORS.
* **Obliczanie Query Port:** Konfiguruje się tylko port gry (np. `2302`). Skrypt automatycznie oblicza Query Port, dodając `+1` (np. `2303`) do żądań API.
* **Bezpośrednie połączenie Steam:** Uruchamia protokół `steam://run/221100//-connect=IP -port=PORT`. Wymusza to na Steam uruchomienie AppID DayZ z parametrami połączenia, pozwalając oficjalnemu launcherowi pobrać wymagane mody. Obsługiwane przez `window.location.href`, aby nie zamykać aktywnej karty.

### Użytkowanie i konfiguracja
1. Pobierz plik `.html`.
2. Otwórz plik w edytorze kodu/tekstu.
3. Znajdź sekcję `<div class="clients-grid">`.
4. Skopiuj i wklej blok `.panel`, aby dodać nowy serwer.
5. Edytuj parametry `data-ip` i `data-game-port` w kodzie karty:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Zapisz zmiany. Panel zaktualizuje informacje wizualne automatycznie po otwarciu.

### Uwagi Techniczne
* **Proxy zewnętrzne:** Zapytania do `dayzsalauncher.com/api/v1/query/` przechodzą przez `api.allorigins.win`. Opóźnienia w ładowaniu wynikają z latencji tej darmowej usługi.
* **Styl wizualny:** Interfejs Dark/Lime z czcionką *Host Grotesk*. Asymetryczny design dedykowany narzędziom client-side.

---

## 🇷🇺 Русский

# Центр подключения клиентов DayZ
Тактическая панель в одном HTML-файле для централизации подключений к серверам клиентов в DayZ. Работает на 100% на стороне клиента, без серверной части, позволяя подключаться к игре в один клик.

### Особенности
* **Один HTML-файл:** CSS и JS встроены. Не требует фреймворков и сборок. Работает при открытии в любом браузере.
* **Данные в реальном времени (DZSA API):** Запрашивает статус сервера (название, карта, онлайн, количество модов) через API DZSA Launcher. Использует публичный прокси (AllOrigins) для обхода блокировок CORS.
* **Расчет Query Port:** Настраивается только игровой порт (например, `2302`). Скрипт автоматически вычисляет Query Port, прибавляя `+1` (например, `2303`) для API-запросов.
* **Прямое подключение Steam:** Выполняет протокол `steam://run/221100//-connect=IP -port=PORT`. Это заставляет Steam запустить AppID DayZ и передать параметры, позволяя официальному лаунчеру скачать нужные моды. Обрабатывается через `window.location.href`, чтобы не закрывать активную вкладку.

### Использование и настройка
1. Скачайте файл `.html`.
2. Откройте файл в любом текстовом редакторе.
3. Найдите раздел `<div class="clients-grid">`.
4. Скопируйте и вставьте блок `.panel`, чтобы добавить новый сервер.
5. Отредактируйте параметры `data-ip` и `data-game-port` в HTML-коде карточки:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Сохраните изменения. Панель обновит данные автоматически при открытии.

### Технические примечания
* **Сторонний прокси:** Запросы к `dayzsalauncher.com/api/v1/query/` проходят через `api.allorigins.win`. Задержки загрузки данных обычно связаны с этим бесплатным сервисом.
* **Визуальный стиль:** Темный интерфейс (Dark/Lime) со шрифтом *Host Grotesk*. Асимметричный дизайн для клиентских инструментов.

---

## 🇧🇷 Português (Brasil)

# Hub de Conexão de Clientes DayZ
Painel tático em um único arquivo HTML para centralizar as conexões aos servidores de clientes no DayZ. Projetado para rodar 100% do lado do cliente, sem necessidade de backend, conectando diretamente ao jogo com um clique.

### Recursos
* **HTML em Arquivo Único:** CSS e JS integrados. Sem frameworks, dependências ou builds. Funciona abrindo o arquivo no navegador.
* **Dados em tempo real (API DZSA):** Consulta o status do servidor (nome, mapa, jogadores online, total de mods) conectando à API do DZSA Launcher. Usa um proxy público (AllOrigins) para evitar bloqueios de CORS.
* **Cálculo de Query Port:** Apenas o port do jogo é configurado (ex. `2302`). O script calcula automaticamente o Query Port somando `+1` (ex. `2303`) para requisições à API.
* **Conexão Direta Steam:** Executa o protocolo `steam://run/221100//-connect=IP -port=PORT`. Isso força o Steam a rodar o AppID do DayZ com os parâmetros de conexão, permitindo ao launcher oficial baixar os mods. Feito via `window.location.href` para não fechar a aba ativa.

### Uso e Configuração
1. Baixe o arquivo `.html`.
2. Abra o arquivo em um editor de código/texto.
3. Busque a seção `<div class="clients-grid">`.
4. Copie e cole o bloco de qualquer `.panel` que representa um servidor para adicionar um novo.
5. Edite os parâmetros `data-ip` e `data-game-port` no HTML do card:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. Salve as alterações. O painel atualizará visualmente ao ser aberto.

### Notas Técnicas
* **Proxy de terceiros:** A consulta a `dayzsalauncher.com/api/v1/query/` requer passar por `api.allorigins.win`. Lentidão no carregamento costuma ser latência desse serviço gratuito.
* **Estilo Visual:** UI Dark/Lime usando a fonte *Host Grotesk*. Design assimétrico para ferramentas client-side.

---

## 🇨🇳 简体中文 (Chino Simplificado)

# DayZ 客户端连接中心
单文件 HTML 战术面板，用于集中管理 DayZ 中的客户端服务器连接。100% 客户端运行，无需后端，一键直连游戏。

### 功能特点
* **单文件 HTML：** 包含内联 CSS 和 JS。无需框架、依赖或构建步骤。在任何浏览器中打开即可运行。
* **实时数据 (DZSA API)：** 连接 DZSA Launcher API 查询服务器状态（名称、地图、在线玩家、Mod 数量）。使用公共代理 (AllOrigins) 绕过 CORS 拦截。
* **查询端口 (Query Port) 计算：** 只需配置游戏端口（如 `2302`）。脚本会自动计算（`+1`）出查询端口（如 `2303`）进行 API 请求。
* **Steam 直连：** 执行 `steam://run/221100//-connect=IP -port=PORT` 协议。强制 Steam 启动 DayZ AppID 并传递连接参数，从而允许官方启动器下载所需的 Mod。通过 `window.location.href` 处理，防止关闭当前标签页。

### 使用与配置
1. 下载 `.html` 文件。
2. 使用任何代码/文本编辑器打开文件。
3. 找到 `<div class="clients-grid">` 部分。
4. 复制并粘贴代表服务器的 `.panel` 模块以添加新服务器。
5. 修改卡片 HTML 中的 `data-ip` 和 `data-game-port` 参数：
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. 保存更改。面板在打开时将自动更新显示信息。

### 技术说明
* **第三方代理：** 访问 `dayzsalauncher.com/api/v1/query/` 必须经过 `api.allorigins.win`。加载延迟通常由该免费桥接服务的延迟引起。
* **视觉风格：** Dark/Lime (黑/酸橙) UI 风格，使用 *Host Grotesk* 字体。针对客户端工具设计的非对称边框。

---

## 🇯🇵 日本語 (Japonés)

# DayZ クライアント接続ハブ
DayZのクライアントサーバー接続を一元化するための、単一ファイルHTMLの戦術パネル。バックエンド不要の100%クライアントサイドで動作し、ワンクリックでゲームに直接接続します。

### 特徴
* **単一ファイルHTML:** CSSとJSを内包。フレームワーク、依存関係、ビルドは一切不要。ブラウザでファイルを開くだけで実行可能。
* **リアルタイムデータ (DZSA API):** DZSA Launcher APIに接続し、サーバー状態（名前、マップ、オンラインプレイヤー、Mod数）を取得。パブリックプロキシ（AllOrigins）を使用してCORSブロックを回避。
* **クエリポートの自動計算:** ゲームポート（例: `2302`）のみを設定。スクリプトがAPIリクエスト用に`+1`（例: `2303`）を加算し、クエリポートを自動計算して使用します。
* **Steamダイレクト接続:** `steam://run/221100//-connect=IP -port=PORT` プロトコルを実行。これによりSteamがDayZのAppIDで起動し、接続パラメータを渡すことで、公式ランチャーが必要なModをダウンロードできるようになります。アクティブなタブが閉じないよう `window.location.href` 経由で処理。

### 使い方と設定
1. `.html` ファイルをダウンロードします。
2. テキスト/コードエディタでファイルを開きます。
3. `<div class="clients-grid">` セクションを探します。
4. サーバーを表す `.panel` ブロックをコピー＆ペーストして、新しいサーバーを追加します。
5. カードのHTML内にある `data-ip` と `data-game-port` パラメータを編集します:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. 変更を保存します。パネルを開くと視覚情報が自動的に更新されます。

### 技術ノート
* **サードパーティプロキシ:** `dayzsalauncher.com/api/v1/query/` へのクエリは `api.allorigins.win` を経由します。データの読み込み遅延は、通常この無料ブリッジサービスのレイテンシによるものです。
* **ビジュアルスタイル:** *Host Grotesk* フォントを使用した Dark/Lime UI。クライアントサイドツール向けの非対称ボーダーデザイン。

---

## 🇰🇷 한국어 (Coreano)

# DayZ 클라이언트 연결 허브
DayZ에서 클라이언트 서버 연결을 중앙 집중화하기 위한 단일 파일 HTML 전술 패널입니다. 백엔드 없이 100% 클라이언트 측에서 실행되며 원클릭으로 게임에 직접 연결할 수 있도록 설계되었습니다.

### 주요 기능
* **단일 파일 HTML:** CSS 및 JS가 통합되어 있습니다. 프레임워크나 빌드가 필요 없습니다. 브라우저에서 파일을 열기만 하면 실행됩니다.
* **실시간 데이터(DZSA API):** DZSA 런처 API에 연결하여 서버 상태(이름, 맵, 접속 플레이어, 모드 수)를 조회합니다. 퍼블릭 프록시(AllOrigins)를 사용하여 CORS 차단을 우회합니다.
* **쿼리 포트(Query Port) 자동 계산:** 게임 포트(예: `2302`)만 구성하면 됩니다. 스크립트가 자동으로 `+1`(예: `2303`)을 더해 API 요청을 위한 쿼리 포트를 계산하고 사용합니다.
* **Steam 직접 연결:** `steam://run/221100//-connect=IP -port=PORT` 프로토콜을 실행합니다. Steam이 DayZ AppID를 실행하고 연결 매개변수를 전달하게 하여 공식 런처가 필요한 모드를 다운로드할 수 있도록 합니다. 활성 탭이 닫히지 않도록 `window.location.href`를 통해 처리됩니다.

### 사용 및 설정
1. `.html` 파일을 다운로드합니다.
2. 텍스트 또는 코드 편집기로 파일을 엽니다.
3. `<div class="clients-grid">` 섹션을 찾습니다.
4. 서버를 나타내는 `.panel` 블록을 복사하여 붙여넣어 새 서버를 추가합니다.
5. 카드의 HTML에서 `data-ip` 및 `data-game-port` 매개변수를 수정합니다:
   ```html
   <div class="panel server-card" data-ip="194.50.234.86" data-game-port="2491">
   ```
6. 변경 사항을 저장합니다. 패널을 열면 시각적 정보가 자동으로 업데이트됩니다.

### 기술 참고 사항
* **타사 프록시:** `dayzsalauncher.com/api/v1/query/`에 대한 쿼리는 `api.allorigins.win`을 거쳐야 합니다. 데이터 로드 지연은 일반적으로 이 무료 브리지 서비스의 지연 시간 때문입니다.
* **시각적 스타일:** *Host Grotesk* 글꼴을 사용한 Dark/Lime UI. 클라이언트 도구에 맞춘 비대칭 테두리 디자인.
