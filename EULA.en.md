# QueryBase End User License Agreement

## 1. Purpose and acceptance

1. This Agreement sets out the terms on which you may use the executable files (including the macOS app, the Windows installer and the Linux AppImage), updates and accompanying documentation (together, the "Software") of "QueryBase", a desktop database client provided by Paldyn (팔딘; "PALDYN", "we" or "us"). The Software is provided for macOS, Windows and Linux, and this Agreement applies to all of them. Where something differs between operating systems, the relevant Section says so, and the supported operating systems, their versions and the supported CPU types are listed in the Public Distribution Repository and the release notes.
2. By installing or using the Software, you agree to this Agreement. If you do not agree, do not install or use the Software.
3. If you use the Software on behalf of a company or other organization, you confirm that you are authorized to accept this Agreement on its behalf.

## 2. Definitions

1. "Public Distribution Repository" means the public repository `paldyn/QueryBase-releases` on GitHub (github.com, operated by GitHub, Inc.; https://github.com/paldyn/QueryBase-releases) in which PALDYN publishes the Software's installers, Updates, release notes and this Agreement.
2. "Update" means a revision, new version or patch of the Software provided by PALDYN.
3. "Paid Features" means features or forms of use of the Software that PALDYN provides for a fee, such as a subscription or a one-time purchase.
4. "Your Databases" means the database servers and database files that you connect to or open with the Software, and the data in them.
5. "Third-Party Components" means open-source software, fonts, icons and other components included in the Software in which third parties hold rights.
6. "Feedback" means comments, suggestions, bug reports and similar input about the Software that you provide to PALDYN.

## 3. License grant

1. Subject to this Agreement, PALDYN grants you a free of charge, non-exclusive, non-transferable, non-sublicensable and revocable license to use the Software.
2. You may use the Software for both personal and commercial purposes, including developing, operating and managing databases for work.
3. This license is limited to installing and using the Software, in the executable form distributed by PALDYN, on devices that you own or lawfully control. No rights in the source code are granted.
4. All rights not expressly granted in this Agreement are reserved by PALDYN.

## 4. Free of charge

1. The Software is provided free of charge for both personal and business use. PALDYN charges no fee for installing, using or updating the Software, and the Software contains no payment function or license key check.
2. PALDYN may introduce Paid Features in the future. If PALDYN introduces Paid Features or reduces what is offered free of charge, it will announce the change and its effective date by a notice in the Public Distribution Repository and in the update release notes at least 30 days before that date.
3. PALDYN will not charge you unless you expressly accept separate paid terms and complete the payment process. Paid Features are governed by those separate paid terms together with this Agreement, and your statutory rights, such as the right to withdraw from a purchase, are governed by those terms and applicable law.
4. The Software works with Your Databases as they are, through the standard means each database provides, and does not convert their data into a format of its own. Whether or not Paid Features are introduced or your license ends, you can therefore keep using Your Databases with other tools.

## 5. Restrictions

You must not:

1. copy the Software beyond what is needed for its normal installation and operation and for backups of your devices, or distribute, redistribute, sell, rent, lease, sublicense or make the Software available to the public;
2. modify, translate or adapt the Software, or create derivative works of it;
3. reverse engineer, decompile or disassemble the Software, or otherwise attempt to derive its source code, except to the extent that applicable law expressly permits this despite this restriction;
4. circumvent, disable or defeat any technical protection or license-management measure of the Software, such as update signature verification, app integrity checks or paid-feature restrictions;
5. remove or alter any copyright, license or trademark notice included in the Software; or
6. use the Software in violation of law or in a way that infringes the rights of others.

## 6. Updates

1. PALDYN may provide Updates but has no obligation to provide Updates or to maintain any particular feature.
2. The Software includes a built-in updater that works as follows:
   1. The Software checks for a new version 30 seconds after it starts and every 24 hours while it is running. You can also check at any time with "Check for Updates…" in the Help menu. There is no setting that turns off these automatic checks.
   2. When it finds a new version that it can install by itself, the Software downloads the Update files in the background without asking you, prepares them for installation and then shows an "Update" button in the bar at the top of the window. There is no setting that turns off this automatic download.
   3. An Update is installed only after you click the "Update" button or choose "Restart and install". Before restarting, the Software checks for work in progress, such as unsaved SQL and uncommitted transactions.
   4. The Software installs only Updates to stable versions and never installs an Update that would go back to an earlier version.
   5. The Software installs only Updates whose signature it can verify with PALDYN's public key built into the Software and that match what was signed, and installs no other Update.
3. You agree that the built-in updater checks for Updates and automatically downloads Update files, and that Updates may be installed as you choose. This Agreement applies to Updates, except where an Update comes with separate terms, in which case those terms apply.
4. PALDYN may stop supporting, or providing Updates for, earlier versions.

## 7. Data practices

1. PALDYN does not use the Software to collect your personal information, the contents of Your Databases, the SQL you run, your connection information, credentials or usage history, or to send them to PALDYN's servers. The Software contains no usage analytics, telemetry, advertising or crash reporting.
2. Update checks and downloads. The only network communications that the Software starts without your request are the update checks and the automatic downloads of Update files described in Section 6.2. Update checks and downloads use HTTPS only: they request the latest release information, the update information files and the update files that PALDYN publishes in the Public Distribution Repository from github.com and GitHub's file servers (release-assets.githubusercontent.com and objects.githubusercontent.com), and no update request goes to any other address. These requests contain no user identifier, account information, connection information or database information added by the Software. As with any internet request, however, ordinary request information, such as your IP address, the time of the request and an identification string (User-Agent) that includes the Software's version and your operating system, reaches GitHub, and the names of the files requested show your operating system and CPU type; this information is handled under GitHub's privacy statement. PALDYN can see the aggregate download count of each file that GitHub provides, which does not identify individual users. Update checks and downloads follow your operating system's proxy settings. On macOS, the downloaded file is passed on for installation through an address used only inside your device (127.0.0.1), and this communication does not leave your device.
3. Database connections. The Software connects to a database server only when you ask it to connect, and connects only to the database servers and SSH servers you enter in a connection's settings and to the addresses to which a database server passes the connection as part of its own connection procedure (for example, an Oracle listener's redirect). While connected, the Software exchanges with that server the SQL you run and the information that the views you open need (for example, the lists and structures of schemas and objects). For authentication it uses the passwords you enter or save, the SSH key and certificate files you choose and the SSH agent running on your device (on Windows, the Windows OpenSSH agent or Pageant). The Software does not reconnect to database servers on its own after it restarts. Information exchanged with a database server, including a cloud database service, is subject to the terms and policies of whoever operates that server.
4. Information stored on your device. The Software stores the following information only on your device and does not send it to PALDYN. The "user data folder" below is `~/Library/Application Support/QueryBase/` on macOS, `%APPDATA%\QueryBase\` on Windows and `$XDG_CONFIG_HOME/QueryBase/` on Linux (`~/.config/QueryBase/` unless set otherwise):
   1. connection settings (the connection's name, database type, host, port, user name, database name (for Oracle, the service name or SID) or SQLite file path, environment and protection level, folder and tags, the SSH server and user name, authentication method, private key file path and the host key fingerprint you accepted, whether TLS is used, the TLS server name, the server certificate DN to check on Oracle connections, and the paths of certificate, key and Oracle wallet files), workspaces and folders, settings (such as language, theme, accent color, density, execution time limits and auto-commit), the document tabs you left open (including unsaved SQL drafts, the paths of the SQL files you opened, and the tables and related-row conditions you opened), layout, the execution history (the SQL run, connection name, start time, duration, row count, outcome, error message and execution settings, such as the row limit and transaction state; kept within the retention you choose, by default the newest 500 per workspace) and favorites, and SQL snippets: in `workspace.json` in the user data folder;
   2. saved passwords: only when you choose to save a connection's password, it is encrypted with a key that your operating system protects (through Electron `safeStorage`, kept by the `QueryBase Safe Storage` item in the keychain on macOS, by DPAPI on Windows and by Secret Service or KWallet on Linux) and stored in `credentials.json` in the user data folder. If that protection is unavailable (including when only the unencrypted `basic_text` method is available on Linux), the password is not saved. SSH passwords and the passphrases of private keys and TLS keys are never saved; they are kept in memory only while connected or until a backup or restore that uses them ends;
   3. work you saved: execution plans (`execution-plans.json`), the list and paths of SQL files you saved or opened (`sql-library.json`), data transfer settings (`transfer-tasks.json`), table filter conditions (`table-condition-presets.json`), diagram layouts (`erd-layouts.json`) and the sample SQLite databases you opened (`databases/`): in the user data folder;
   4. window position and size: in `window-state.json` in the user data folder;
   5. a diagnostic log (the app version and operating system at start, starts and quits, abnormal exits of the window or of worker processes, the kind and error code of failed requests, the reasons why update checks or installations failed, and the like; SQL, data values and passwords are never recorded): in `logs/` in the user data folder (1 MiB per file, at most 3 files);
   6. temporary working files: files that hold query results and data being transferred while you page through, export or transfer results (in `query-result-cache/` in the user data folder), and the temporary folder used during a backup or restore (in the folder of the backup file or in the operating system's temporary folder). They are deleted when the work ends or the results are no longer needed. They can remain if the Software ends abnormally; files left in `query-result-cache/` are deleted the next time it runs;
   7. update files: the Update files that the Software downloaded automatically are stored on macOS in `~/Library/Caches/querybase-updater/` and, for preparing Updates for installation, in `~/Library/Caches/com.paldyn.querybase/` and `~/Library/Caches/com.paldyn.querybase.ShipIt/`, with `~/Library/HTTPStorages/com.paldyn.querybase/`, which macOS's networking components create while an Update is prepared; on Windows in `%LOCALAPPDATA%\querybase-updater\`; and on Linux in `$XDG_CACHE_HOME/querybase-updater/` (`~/.cache/querybase-updater/` unless set otherwise). These files stay on your device if you do not install the Update, and are used at the next start without downloading them again or are replaced by the files of a newer version. The Windows installer also leaves a copy of itself (`installer.exe`) in `%LOCALAPPDATA%\querybase-updater\` at every installation; and
   8. technical files, such as the caches that Electron uses to draw the window: in the user data folder. On macOS, `~/Library/Preferences/com.paldyn.querybase.plist` is created as well.

   This information may remain on your device after you delete the Software. You can delete the files in the locations above yourself. The Windows uninstaller deletes neither the user data folder nor `%LOCALAPPDATA%\querybase-updater\`. On macOS you can also delete the `QueryBase Safe Storage` item in Keychain Access. Deleting the user data folder also deletes your saved connections and passwords and your unsaved SQL drafts.

5. Other local integrations. When you ask it to, the Software opens the files you choose (such as SQLite databases, SQL and CSV files, backup files, connection settings files, and SSH key and certificate files) or saves files where you choose, copies text to the clipboard, opens the logs folder in Finder (File Explorer on Windows, the file manager on Linux) and opens the notices file of the Third-Party Components in your operating system's default application. When an Update cannot be checked or installed and you click "Open Download Page", it opens the releases page of the Public Distribution Repository in your default browser. When you ask for a backup or restore of a server database, the Software runs, on your device, the database vendor's command-line tool that you installed and chose (for example `pg_dump`, `mysqldump` or `expdp`) and passes the connection details and password that the run needs only to that tool, through its environment variables or standard input. That tool connects to the database server entered in the connection's settings.
6. If PALDYN intends to process information differently from this Section, for example for license checks of Paid Features, it will first amend this Agreement, announce the change by a notice in the Public Distribution Repository and in the update release notes and, where applicable law requires, obtain your consent.

## 8. Ownership

1. The Software is licensed, not sold. All intellectual property rights in the Software, its copies and Updates, including copyrights, patents, trademarks and trade secrets, belong to PALDYN or its licensors.
2. Rights in Your Databases and in the SQL, files and other content you work with in the Software remain with you or their rightful owners, and PALDYN acquires no rights in that content under this Agreement.

## 9. Feedback

1. You are not required to provide Feedback.
2. If you provide Feedback, PALDYN has a worldwide, perpetual, irrevocable and royalty-free right to use, modify, publish and commercialize it in the Software and in PALDYN's products and services, without payment or attribution to you.
3. Do not include confidential information or content in which others hold rights in your Feedback. In particular, anyone can read what you post in the issues of the Public Distribution Repository, so never include passwords, connection information or real data there. PALDYN has no duty of confidentiality regarding Feedback; however, personal information provided with Feedback is handled in accordance with applicable law.

## 10. Third-party components and services

1. The Software includes Third-Party Components, such as Electron (including Chromium and Node.js) and npm packages. The list and full license texts of the npm packages are in `THIRD_PARTY_NOTICES.txt`, and the license notices of Electron and Chromium and the notices of the database icons are in the `licenses` folder, all provided with the Software (in the macOS app, in `Contents/Resources/`; on Windows, in `resources\` in the installation folder; on Linux, in `resources/` inside the AppImage). You can open `THIRD_PARTY_NOTICES.txt` with "Third-party Licenses…" in the Help menu. Third-Party Components are governed by their own licenses, and nothing in this Agreement, including Section 5, limits the rights you have under those licenses.
2. Services operated by third parties, such as GitHub, and the database services you connect to are governed by those third parties' terms. PALDYN is not responsible for the availability, content or information handling of third-party services.
3. The names and logos of PostgreSQL, MySQL, MariaDB, SQLite, Oracle and SQL Server shown in the Software are trademarks of their respective owners and are used only to identify the supported kinds of database. Their use does not imply any affiliation with, sponsorship by or endorsement by those owners.
4. The database vendors' command-line tools used to back up and restore server databases are not part of the Software, and the Software does not download them. The tools you obtain from each vendor and install are governed by that vendor's license and terms.

## 11. Disclaimer of warranties

1. The Software may contain errors, defects or missing features, and its features may change through Updates without notice.
2. The Software is provided "AS IS" and "AS AVAILABLE". To the maximum extent permitted by applicable law, PALDYN makes no warranties of any kind, express or implied, including warranties of merchantability, fitness for a particular purpose, non-infringement, accuracy and uninterrupted operation.
3. Running SQL in the Software, editing results and table data, creating, changing or deleting tables and other objects, importing and transferring data, restoring, ending sessions and changing users and privileges change Your Databases and may be irreversible. Changes made in auto-commit mode take effect immediately. The Software's environment labels, protection levels and change reviews and confirmations are meant to reduce mistakes and do not guarantee that every error or loss is prevented. You are responsible for checking what a change does and what it applies to before you run it against Your Databases, and you should back up important data regularly.
4. This Section does not apply to any of your rights that cannot be excluded or limited under applicable law. Any part of this Section that is invalid under the Act on the Regulation of Terms and Conditions of the Republic of Korea or other applicable law does not apply, and applicable law governs that part instead.

## 12. Limitation of liability

1. To the maximum extent permitted by applicable law, PALDYN is not liable for any indirect, special, incidental, consequential or punitive damages, or for any loss of profits, revenue, data or business opportunities, arising from the use of or inability to use the Software, whether or not PALDYN was aware of the possibility of such damages.
2. To the maximum extent permitted by applicable law, PALDYN's total liability arising from or relating to this Agreement or the Software will not exceed the greater of the amount you paid PALDYN to use the Software and KRW 100,000.
3. Sections 12.1 and 12.2 do not apply to damages caused by PALDYN's willful misconduct or gross negligence, to damages to life or physical health, or in any other case in which liability cannot be excluded or limited under applicable law. Any part of this Section that is invalid under the Act on the Regulation of Terms and Conditions of the Republic of Korea or other applicable law does not apply, and applicable law governs that part instead.

## 13. Term and termination

1. This Agreement takes effect when you install or use the Software and remains in effect until terminated.
2. You may terminate this Agreement at any time by ceasing to use the Software and deleting all copies of it.
3. If you materially breach this Agreement, PALDYN may terminate your license immediately by notifying you.
4. PALDYN may end the license, for reasons such as the discontinuation of the Software, after announcing it by a notice in the Public Distribution Repository and in the update release notes at least 30 days in advance. The introduction of Paid Features and changes to what is offered free of charge are governed by Section 4.
5. When your license ends, you must stop using the Software and delete all copies of it. Your Databases remain intact, and you can keep using them with other tools.
6. Sections 5, 8 to 12, 15 and 16 survive termination of this Agreement.

## 14. Changes to this Agreement

1. PALDYN may change this Agreement to the extent permitted by applicable law.
2. PALDYN will announce the changes and their effective date by a notice in the Public Distribution Repository and in the update release notes at least 30 days before that date.
3. If you continue to use the Software after the effective date of the changed Agreement, you are deemed to have accepted the changes. If you do not accept them, you may stop using the Software and terminate this Agreement.

## 15. Governing law and jurisdiction

1. This Agreement is governed by and construed in accordance with the laws of the Republic of Korea.
2. The court with jurisdiction over disputes arising from or relating to this Agreement or the Software is determined under the Civil Procedure Act of the Republic of Korea and other applicable law.

## 16. General

1. This Agreement is the entire agreement between you and PALDYN regarding the Software and supersedes any prior agreement or representation on that subject, except that separate terms for Paid Features apply to those features.
2. If any provision of this Agreement is invalid or unenforceable, the remaining provisions remain in effect.
3. PALDYN's failure or delay in exercising a right under this Agreement is not a waiver of that right.
4. You may not assign this Agreement or your rights under it without PALDYN's prior written consent. PALDYN may transfer its position under this Agreement in connection with a merger, business transfer or similar transaction.
5. This Agreement is written in Korean and English. If the two versions differ, the Korean version prevails.

## 17. Contact

For questions about this Agreement or the Software, contact:

- Company: Paldyn (팔딘)
- Representative: Wonmo Lee (이원모)
- Email: support@paldyn.com

## Effective date

1. This Agreement takes effect on 3 November 2026.
2. The amendments to Sections 6.2.2, 6.2.3, 6.3, 7.2 and 7.4.7 take effect on 5 November 2026.
