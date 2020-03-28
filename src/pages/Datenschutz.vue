<template>
  <Layout>

    <div class="min-h-screen bg-white">
      <nav class="bg-white border-b border-gray-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div class="flex justify-between h-16">
            <div class="flex">
              <div class="flex-shrink-0 flex items-center">
                <img class="block h-8 w-auto" src="/img/logos/workflow-mark-on-white.svg" alt="Workflow logo" />
              </div>
              <div class="hidden sm:-my-px sm:ml-6 sm:flex">
                <a href="#" class="inline-flex items-center px-1 pt-1 border-b-2 border-indigo-500 text-sm font-medium leading-5 text-gray-900 focus:outline-none focus:border-indigo-700 transition duration-150 ease-in-out">
                  Dashboard
                </a>
                <a href="#" class="ml-8 inline-flex items-center px-1 pt-1 border-b-2 border-transparent text-sm font-medium leading-5 text-gray-500 hover:text-gray-700 hover:border-gray-300 focus:outline-none focus:text-gray-700 focus:border-gray-300 transition duration-150 ease-in-out">
                  Team
                </a>
                <a href="#" class="ml-8 inline-flex items-center px-1 pt-1 border-b-2 border-transparent text-sm font-medium leading-5 text-gray-500 hover:text-gray-700 hover:border-gray-300 focus:outline-none focus:text-gray-700 focus:border-gray-300 transition duration-150 ease-in-out">
                  Projects
                </a>
                <a href="#" class="ml-8 inline-flex items-center px-1 pt-1 border-b-2 border-transparent text-sm font-medium leading-5 text-gray-500 hover:text-gray-700 hover:border-gray-300 focus:outline-none focus:text-gray-700 focus:border-gray-300 transition duration-150 ease-in-out">
                  Calendar
                </a>
              </div>
            </div>
            <div class="hidden sm:ml-6 sm:flex sm:items-center">
              <button class="p-1 border-2 border-transparent text-gray-400 rounded-full hover:text-gray-500 focus:outline-none focus:text-gray-500 focus:bg-gray-100 transition duration-150 ease-in-out" aria-label="Notifications">
                <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" />
                </svg>
              </button>
              <div class="ml-3 relative">
                <div>
                  <button @click="toggle" class="flex text-sm border-2 border-transparent rounded-full focus:outline-none focus:border-gray-300 transition duration-150 ease-in-out" id="user-menu" aria-label="User menu" aria-haspopup="true" x-bind:aria-expanded="open">
                    <img class="h-8 w-8 rounded-full" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="" />
                  </button>
                </div>
                <div x-show="open" x-transition:enter="transition ease-out duration-200" x-transition:enter-start="transform opacity-0 scale-95" x-transition:enter-end="transform opacity-100 scale-100" x-transition:leave="transition ease-in duration-75" x-transition:leave-start="transform opacity-100 scale-100" x-transition:leave-end="transform opacity-0 scale-95" class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg">
                  <div class="py-1 rounded-md bg-white shadow-xs">
                    <a href="#" class="block px-4 py-2 text-sm leading-5 text-gray-700 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 transition duration-150 ease-in-out">Your Profile</a>
                    <a href="#" class="block px-4 py-2 text-sm leading-5 text-gray-700 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 transition duration-150 ease-in-out">Settings</a>
                    <a href="#" class="block px-4 py-2 text-sm leading-5 text-gray-700 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 transition duration-150 ease-in-out">Sign out</a>
                  </div>
                </div>
              </div>
            </div>
            <div class="-mr-2 flex items-center sm:hidden">
              <button @click="open = !open" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500 transition duration-150 ease-in-out" x-bind:aria-label="open ? 'Close main menu' : 'Main menu'" x-bind:aria-expanded="open">
                <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                  <path :class="{'hidden': open, 'inline-flex': !open }" class="inline-flex" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                  <path :class="{'hidden': !open, 'inline-flex': open }" class="hidden" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                </svg>
              </button>
            </div>
          </div>
        </div>
        <div :class="{'block': open, 'hidden': !open}" class="hidden sm:hidden">
          <div class="pt-2 pb-3">
            <a href="#" class="block pl-3 pr-4 py-2 border-l-4 border-indigo-500 text-base font-medium text-indigo-700 bg-indigo-50 focus:outline-none focus:text-indigo-800 focus:bg-indigo-100 focus:border-indigo-700 transition duration-150 ease-in-out">Dashboard</a>
            <a href="#" class="mt-1 block pl-3 pr-4 py-2 border-l-4 border-transparent text-base font-medium text-gray-600 hover:text-gray-800 hover:bg-gray-50 hover:border-gray-300 focus:outline-none focus:text-gray-800 focus:bg-gray-50 focus:border-gray-300 transition duration-150 ease-in-out">Team</a>
            <a href="#" class="mt-1 block pl-3 pr-4 py-2 border-l-4 border-transparent text-base font-medium text-gray-600 hover:text-gray-800 hover:bg-gray-50 hover:border-gray-300 focus:outline-none focus:text-gray-800 focus:bg-gray-50 focus:border-gray-300 transition duration-150 ease-in-out">Projects</a>
            <a href="#" class="mt-1 block pl-3 pr-4 py-2 border-l-4 border-transparent text-base font-medium text-gray-600 hover:text-gray-800 hover:bg-gray-50 hover:border-gray-300 focus:outline-none focus:text-gray-800 focus:bg-gray-50 focus:border-gray-300 transition duration-150 ease-in-out">Calendar</a>
          </div>
          <div class="pt-4 pb-3 border-t border-gray-200">
            <div class="flex items-center px-4">
              <div class="flex-shrink-0">
                <img class="h-10 w-10 rounded-full" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="" />
              </div>
              <div class="ml-3">
                <div class="text-base font-medium leading-6 text-gray-800">Tom Cook</div>
                <div class="text-sm font-medium leading-5 text-gray-500">tom@example.com</div>
              </div>
            </div>
            <div class="mt-3" role="menu" aria-orientation="vertical" aria-labelledby="user-menu">
              <a href="#" class="block px-4 py-2 text-base font-medium text-gray-500 hover:text-gray-800 hover:bg-gray-100 focus:outline-none focus:text-gray-800 focus:bg-gray-100 transition duration-150 ease-in-out" role="menuitem">Your Profile</a>
              <a href="#" class="mt-1 block px-4 py-2 text-base font-medium text-gray-500 hover:text-gray-800 hover:bg-gray-100 focus:outline-none focus:text-gray-800 focus:bg-gray-100 transition duration-150 ease-in-out" role="menuitem">Settings</a>
              <a href="#" class="mt-1 block px-4 py-2 text-base font-medium text-gray-500 hover:text-gray-800 hover:bg-gray-100 focus:outline-none focus:text-gray-800 focus:bg-gray-100 transition duration-150 ease-in-out" role="menuitem">Sign out</a>
            </div>
          </div>
        </div>
      </nav>

      <div class="py-10">
        <main>
          <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">

            <!-- Datenschutz -->
            <div class="px-4 py-8 sm:px-0">
              

    <div class="text-gray-600 container max-w-3xl mx-auto font-copy text-lg">
      <h1 class="text-4xl mt-16 font-bold">Datenschutzerklärung</h1>
      <h2 class="text-xl mt-16 font-bold" id="m14">Einleitung</h2>
      <p class="mt-4">
        Mit der folgenden Datenschutzerklärung möchten wir Sie darüber
        aufklären, welche Arten Ihrer personenbezogenen Daten (nachfolgend auch
        kurz als "Daten“ bezeichnet) wir zu welchen Zwecken und in welchem
        Umfang verarbeiten. Die Datenschutzerklärung gilt für alle von uns
        durchgeführten Verarbeitungen personenbezogener Daten, sowohl im Rahmen
        der Erbringung unserer Leistungen als auch insbesondere auf unseren
        Webseiten, in mobilen Applikationen sowie innerhalb externer
        Onlinepräsenzen, wie z.B. unserer Social-Media-Profile (nachfolgend
        zusammenfassend bezeichnet als "Onlineangebot“).
      </p>
      <p class="mt-4">Die verwendeten Begriffe sind nicht geschlechtsspezifisch.</p>
      <ul class="list-disc mt-4"></ul>
      <p class="mt-4">Stand: 28.03.2020</p>
      <h2 class="text-xl mt-16 font-bold">Inhaltsübersicht</h2>
      <ul class="list-disc mt-4">
        <li><a href="#m14"> Einleitung</a></li>
        <li><a href="#m3"> Verantwortlicher</a></li>
        <li>
          <a href="#mOverview">
            Übersicht der Verarbeitungen</a
          >
        </li>
        <li>
          <a href="#m13"> Maßgebliche Rechtsgrundlagen</a>
        </li>
        <li><a href="#m27"> Sicherheitsmaßnahmen</a></li>
        <li>
          <a href="#m25">
            Übermittlung und Offenbarung von personenbezogenen Daten</a
          >
        </li>
        <li>
          <a href="#m24">
            Datenverarbeitung in Drittländern</a
          >
        </li>
        <li><a href="#m134"> Einsatz von Cookies</a></li>
        <li>
          <a href="#m225">
            Bereitstellung des Onlineangebotes und Webhosting</a
          >
        </li>
        <li>
          <a href="#m17">
            Newsletter und Breitenkommunikation</a
          >
        </li>
        <li><a href="#m12"> Löschung von Daten</a></li>
        <li>
          <a href="#m15">
            Änderung und Aktualisierung der Datenschutzerklärung</a
          >
        </li>
        <li>
          <a href="#m10"> Rechte der betroffenen Personen</a>
        </li>
        <li><a href="#m42"> Begriffsdefinitionen</a></li>
      </ul>
      <h2 class="text-xl mt-16 font-bold" id="m3">Verantwortlicher</h2>
      <p class="mt-4">Inviado Ltd & Co KG<br />wie im Impressum angegeben: 
        <a href="https://blankenese.online/impressum">https://blankenese.online/impressum</a>
      </p>
      <p class="mt-4">
        <strong>Vertretungsberechtigte Personen</strong>: Jan Prill,
        Babendiekstr. 60b, 22587 Hamburg
      </p>
      <p class="mt-4">
        <strong>E-Mail-Adresse</strong>:
        <a href="mailto:jan.prill@inviado.com">jan.prill@inviado.com</a>
      </p>
      <p class="mt-4">
        <strong>Impressum</strong>:
        <a href="https://blankenese.online/impressum" target="_blank"
          >https://blankenese.online/impressum</a
        >
      </p>
      <ul class="list-disc mt-4"></ul>
      <h2 class="text-xl mt-16 font-bold" id="mOverview">Übersicht der Verarbeitungen</h2>
      <p class="mt-4">
        Die nachfolgende Übersicht fasst die Arten der verarbeiteten Daten und
        die Zwecke ihrer Verarbeitung zusammen und verweist auf die betroffenen
        Personen.
      </p>
      <h3>Arten der verarbeiteten Daten</h3>
      <ul class="list-disc mt-4">
        <li><p class="mt-4">Bestandsdaten (z.B. Namen, Adressen).</p></li>
        <li><p class="mt-4">Inhaltsdaten (z.B. Texteingaben, Fotografien, Videos).</p></li>
        <li><p class="mt-4">Kontaktdaten (z.B. E-Mail, Telefonnummern).</p></li>
        <li>
          <p class="mt-4">
            Meta-/Kommunikationsdaten (z.B. Geräte-Informationen, IP-Adressen).
          </p>
        </li>
        <li>
          <p class="mt-4">
            Nutzungsdaten (z.B. besuchte Webseiten, Interesse an Inhalten,
            Zugriffszeiten).
          </p>
        </li>
      </ul>
      <h3>Kategorien betroffener Personen</h3>
      <ul class="list-disc mt-4">
        <li><p class="mt-4">Kommunikationspartner.</p></li>
        <li>
          <p class="mt-4">Nutzer (z.B. Webseitenbesucher, Nutzer von Onlinediensten).</p>
        </li>
      </ul>
      <h3>Zwecke der Verarbeitung</h3>
      <ul class="list-disc mt-4">
        <li><p class="mt-4">Content Delivery Network (CDN).</p></li>
        <li><p class="mt-4">Direktmarketing (z.B. per E-Mail oder postalisch).</p></li>
        <li><p class="mt-4">Vertragliche Leistungen und Service.</p></li>
      </ul>
      <h2>Rechtsgrundlagen</h2>
      <h3 id="m13">Maßgebliche Rechtsgrundlagen</h3>
      <p class="mt-4">
        Im Folgenden teilen wir die Rechtsgrundlagen der
        Datenschutzgrundverordnung (DSGVO), auf deren Basis wir die
        personenbezogenen Daten verarbeiten, mit. Bitte beachten Sie, dass
        zusätzlich zu den Regelungen der DSGVO die nationalen
        Datenschutzvorgaben in Ihrem bzw. unserem Wohn- und Sitzland gelten
        können.
      </p>
      <ul class="list-disc mt-4">
        <li>
          <p class="mt-4">
            <strong>Einwilligung (Art. 6 Abs. 1 S. 1 lit. a DSGVO)</strong> -
            Die betroffene Person hat ihre Einwilligung in die Verarbeitung der
            sie betreffenden personenbezogenen Daten für einen spezifischen
            Zweck oder mehrere bestimmte Zwecke gegeben.
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f. DSGVO)</strong>
            - Die Verarbeitung ist zur Wahrung der berechtigten Interessen des
            Verantwortlichen oder eines Dritten erforderlich, sofern nicht die
            Interessen oder Grundrechte und Grundfreiheiten der betroffenen
            Person, die den Schutz personenbezogener Daten erfordern,
            überwiegen.
          </p>
        </li>
      </ul>
      <p class="mt-4">
        <strong>Nationale Datenschutzregelungen in Deutschland</strong>:
        Zusätzlich zu den Datenschutzregelungen der Datenschutz-Grundverordnung
        gelten nationale Regelungen zum Datenschutz in Deutschland. Hierzu
        gehört insbesondere das Gesetz zum Schutz vor Missbrauch
        personenbezogener Daten bei der Datenverarbeitung
        (Bundesdatenschutzgesetz – BDSG). Das BDSG enthält insbesondere
        Spezialregelungen zum Recht auf Auskunft, zum Recht auf Löschung, zum
        Widerspruchsrecht, zur Verarbeitung besonderer Kategorien
        personenbezogener Daten, zur Verarbeitung für andere Zwecke und zur
        Übermittlung sowie automatisierten Entscheidungsfindung im Einzelfall
        einschließlich Profiling. Des Weiteren regelt es die Datenverarbeitung
        für Zwecke des Beschäftigungsverhältnisses (§ 26 BDSG), insbesondere im
        Hinblick auf die Begründung, Durchführung oder Beendigung von
        Beschäftigungsverhältnissen sowie die Einwilligung von Beschäftigten.
        Ferner können Landesdatenschutzgesetze der einzelnen Bundesländer zur
        Anwendung gelangen.
      </p>
      <ul class="list-disc mt-4"></ul>
      <h2 class="text-xl mt-16 font-bold" id="m27">Sicherheitsmaßnahmen</h2>
      <p class="mt-4">
        Wir treffen nach Maßgabe der gesetzlichen Vorgaben unter
        Berücksichtigung des Stands der Technik, der Implementierungskosten und
        der Art, des Umfangs, der Umstände und der Zwecke der Verarbeitung sowie
        der unterschiedlichen Eintrittswahrscheinlichkeiten und des Ausmaßes der
        Bedrohung der Rechte und Freiheiten natürlicher Personen geeignete
        technische und organisatorische Maßnahmen, um ein dem Risiko
        angemessenes Schutzniveau zu gewährleisten.
      </p>
      <p class="mt-4">
        Zu den Maßnahmen gehören insbesondere die Sicherung der Vertraulichkeit,
        Integrität und Verfügbarkeit von Daten durch Kontrolle des physischen
        und elektronischen Zugangs zu den Daten als auch des sie betreffenden
        Zugriffs, der Eingabe, der Weitergabe, der Sicherung der Verfügbarkeit
        und ihrer Trennung. Des Weiteren haben wir Verfahren eingerichtet, die
        eine Wahrnehmung von Betroffenenrechten, die Löschung von Daten und
        Reaktionen auf die Gefährdung der Daten gewährleisten. Ferner
        berücksichtigen wir den Schutz personenbezogener Daten bereits bei der
        Entwicklung bzw. Auswahl von Hardware, Software sowie Verfahren
        entsprechend dem Prinzip des Datenschutzes, durch Technikgestaltung und
        durch datenschutzfreundliche Voreinstellungen.
      </p>
      <p class="mt-4">
        <strong>SSL-Verschlüsselung (https)</strong>: Um Ihre via unser
        Online-Angebot übermittelten Daten zu schützen, nutzen wir eine
        SSL-Verschlüsselung. Sie erkennen derart verschlüsselte Verbindungen an
        dem Präfix https:// in der Adresszeile Ihres Browsers.
      </p>
      <h2 class="text-xl mt-16 font-bold" id="m25">Übermittlung und Offenbarung von personenbezogenen Daten</h2>
      <p class="mt-4">
        Im Rahmen unserer Verarbeitung von personenbezogenen Daten kommt es vor,
        dass die Daten an andere Stellen, Unternehmen, rechtlich selbstständige
        Organisationseinheiten oder Personen übermittelt oder sie ihnen
        gegenüber offengelegt werden. Zu den Empfängern dieser Daten können z.B.
        Zahlungsinstitute im Rahmen von Zahlungsvorgängen, mit IT-Aufgaben
        beauftragte Dienstleister oder Anbieter von Diensten und Inhalten, die
        in eine Webseite eingebunden werden, gehören. In solchen Fall beachten
        wir die gesetzlichen Vorgaben und schließen insbesondere entsprechende
        Verträge bzw. Vereinbarungen, die dem Schutz Ihrer Daten dienen, mit den
        Empfängern Ihrer Daten ab.
      </p>
      <h2 class="text-xl mt-16 font-bold" id="m24">Datenverarbeitung in Drittländern</h2>
      <p class="mt-4">
        Sofern wir Daten in einem Drittland (d.h., außerhalb der Europäischen
        Union (EU), des Europäischen Wirtschaftsraums (EWR)) verarbeiten oder
        die Verarbeitung im Rahmen der Inanspruchnahme von Diensten Dritter oder
        der Offenlegung bzw. Übermittlung von Daten an andere Personen, Stellen
        oder Unternehmen stattfindet, erfolgt dies nur im Einklang mit den
        gesetzlichen Vorgaben.
      </p>
      <p class="mt-4">
        Vorbehaltlich ausdrücklicher Einwilligung oder vertraglich oder
        gesetzlich erforderlicher Übermittlung verarbeiten oder lassen wir die
        Daten nur in Drittländern mit einem anerkannten Datenschutzniveau, zu
        denen die unter dem "Privacy-Shield" zertifizierten US-Verarbeiter
        gehören, oder auf Grundlage besonderer Garantien, wie z.B. vertraglicher
        Verpflichtung durch sogenannte Standardschutzklauseln der EU-Kommission,
        des Vorliegens von Zertifizierungen oder verbindlicher interner
        Datenschutzvorschriften, verarbeiten (Art. 44 bis 49 DSGVO,
        Informationsseite der EU-Kommission:
        <a
          href="https://ec.europa.eu/info/law/law-topic/data-protection/international-dimension-data-protection_de"
          target="_blank"
          >https://ec.europa.eu/info/law/law-topic/data-protection/international-dimension-data-protection_de</a
        >
        ).
      </p>
      <h2 class="text-xl mt-16 font-bold" id="m134">Einsatz von Cookies</h2>
      <p class="mt-4">
        Auf dieser Website (blankenese.online) werden KEINE cookies eingesetzt. Es ist aber nicht ausgeschlossen,
        dass Drittanbieter Cookies einsetzen. Deswegen informiere ich Sie im folgenden Abschnitt, allgemein 
        über Cookies.
      </p>
      <p class="mt-4">
        Cookies sind Textdateien, die Daten von besuchten Websites oder Domains
        enthalten und von einem Browser auf dem Computer des Benutzers
        gespeichert werden. Ein Cookie dient in erster Linie dazu, die
        Informationen über einen Benutzer während oder nach seinem Besuch
        innerhalb eines Onlineangebotes zu speichern. Zu den gespeicherten
        Angaben können z.B. die Spracheinstellungen auf einer Webseite, der
        Loginstatus, ein Warenkorb oder die Stelle, an der ein Video geschaut
        wurde, gehören. Zu dem Begriff der Cookies zählen wir ferner andere
        Technologien, die die gleichen Funktionen wie Cookies erfüllen (z.B.,
        wenn Angaben der Nutzer anhand pseudonymer Onlinekennzeichnungen
        gespeichert werden, auch als "Nutzer-IDs" bezeichnet)
      </p>
      <p class="mt-4">
        <strong
          >Die folgenden Cookie-Typen und Funktionen werden
          unterschieden:</strong
        >
      </p>
      <ul class="list-disc mt-4">
        <li>
          <strong
            >Temporäre Cookies (auch: Session- oder Sitzungs-Cookies):</strong
          >
          Temporäre Cookies werden spätestens gelöscht, nachdem ein Nutzer ein
          Online-Angebot verlassen und seinen Browser geschlossen hat.
        </li>
        <li>
          <strong>Permanente Cookies:</strong> Permanente Cookies bleiben auch
          nach dem Schließen des Browsers gespeichert. So kann beispielsweise
          der Login-Status gespeichert oder bevorzugte Inhalte direkt angezeigt
          werden, wenn der Nutzer eine Website erneut besucht. Ebenso können die
          Interessen von Nutzern, die zur Reichweitenmessung oder zu
          Marketingzwecken verwendet werden, in einem solchen Cookie gespeichert
          werden.
        </li>
        <li>
          <strong>First-Party-Cookies:</strong> First-Party-Cookies werden von
          uns selbst gesetzt.
        </li>
        <li>
          <strong>Third-Party-Cookies (auch: Drittanbieter-Cookies)</strong>:
          Drittanbieter-Cookies werden hauptsächlich von Werbetreibenden (sog.
          Dritten) verwendet, um Benutzerinformationen zu verarbeiten.
        </li>
        <li>
          <strong
            >Notwendige (auch: essentielle oder unbedingt erforderliche)
            Cookies:</strong
          >
          Cookies können zum einen für den Betrieb einer Webseite unbedingt
          erforderlich sein (z.B. um Logins oder andere Nutzereingaben zu
          speichern oder aus Gründen der Sicherheit).
        </li>
        <li>
          <strong>Statistik-, Marketing- und Personalisierungs-Cookies</strong>:
          Ferner werden Cookies im Regelfall auch im Rahmen der
          Reichweitenmessung eingesetzt sowie dann, wenn die Interessen eines
          Nutzers oder sein Verhalten (z.B. Betrachten bestimmter Inhalte,
          Nutzen von Funktionen etc.) auf einzelnen Webseiten in einem
          Nutzerprofil gespeichert werden. Solche Profile dienen dazu, den
          Nutzern z.B. Inhalte anzuzeigen, die ihren potentiellen Interessen
          entsprechen. Dieses Verfahren wird auch als "Tracking", d.h.,
          Nachverfolgung der potentiellen Interessen der Nutzer bezeichnet. .
          Soweit wir Cookies oder "Tracking"-Technologien einsetzen, informieren
          wir Sie gesondert in unserer Datenschutzerklärung oder im Rahmen der
          Einholung einer Einwilligung.
        </li>
      </ul>
      <p class="mt-4">
        <strong>Hinweise zu Rechtsgrundlagen: </strong> Auf welcher
        Rechtsgrundlage wir Ihre personenbezogenen Daten mit Hilfe von Cookies
        verarbeiten, hängt davon ab, ob wir Sie um eine Einwilligung bitten.
        Falls dies zutrifft und Sie in die Nutzung von Cookies einwilligen, ist
        die Rechtsgrundlage der Verarbeitung Ihrer Daten die erklärte
        Einwilligung. Andernfalls werden die mithilfe von Cookies verarbeiteten
        Daten auf Grundlage unserer berechtigten Interessen (z.B. an einem
        betriebswirtschaftlichen Betrieb unseres Onlineangebotes und dessen
        Verbesserung) verarbeitet oder, wenn der Einsatz von Cookies
        erforderlich ist, um unsere vertraglichen Verpflichtungen zu erfüllen.
      </p>
      <p class="mt-4">
        <strong
          >Allgemeine Hinweise zum Widerruf und Widerspruch (Opt-Out):
        </strong>
        Abhängig davon, ob die Verarbeitung auf Grundlage einer Einwilligung
        oder gesetzlichen Erlaubnis erfolgt, haben Sie jederzeit die
        Möglichkeit, eine erteilte Einwilligung zu widerrufen oder der
        Verarbeitung Ihrer Daten durch Cookie-Technologien zu widersprechen
        (zusammenfassend als "Opt-Out" bezeichnet). Sie können Ihren Widerspruch
        zunächst mittels der Einstellungen Ihres Browsers erklären, z.B., indem
        Sie die Nutzung von Cookies deaktivieren (wobei hierdurch auch die
        Funktionsfähigkeit unseres Onlineangebotes eingeschränkt werden kann).
        Ein Widerspruch gegen den Einsatz von Cookies zu Zwecken des
        Onlinemarketings kann auch mittels einer Vielzahl von Diensten, vor
        allem im Fall des Trackings, über die Webseiten
        <a href="http://optout.aboutads.info" target="_blank"
          >http://optout.aboutads.info</a
        >
        und
        <a href="http://www.youronlinechoices.com/" target="_blank"
          >http://www.youronlinechoices.com/</a
        >
        erklärt werden. Daneben können Sie weitere Widerspruchshinweise im
        Rahmen der Angaben zu den eingesetzten Dienstleistern und Cookies
        erhalten.
      </p>
      <p class="mt-4">
        <strong
          >Verarbeitung von Cookie-Daten auf Grundlage einer
          Einwilligung</strong
        >: Bevor wir Daten im Rahmen der Nutzung von Cookies verarbeiten oder
        verarbeiten lassen, bitten wir die Nutzer um eine jederzeit widerrufbare
        Einwilligung. Bevor die Einwilligung nicht ausgesprochen wurde, werden
        allenfalls Cookies eingesetzt, die für den Betrieb unseres
        Onlineangebotes erforderlich sind. Deren Einsatz erfolgt auf der
        Grundlage unseres Interesses und des Interesses der Nutzer an der
        erwarteten Funktionsfähigkeit unseres Onlineangebotes.
      </p>
      <ul class="list-disc mt-4">
        <li>
          <p class="mt-4">
            <strong>Verarbeitete Datenarten:</strong> Nutzungsdaten (z.B.
            besuchte Webseiten, Interesse an Inhalten, Zugriffszeiten),
            Meta-/Kommunikationsdaten (z.B. Geräte-Informationen, IP-Adressen).
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Betroffene Personen:</strong> Nutzer (z.B.
            Webseitenbesucher, Nutzer von Onlinediensten).
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Rechtsgrundlagen:</strong> Einwilligung (Art. 6 Abs. 1 S. 1
            lit. a DSGVO), Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f.
            DSGVO).
          </p>
        </li>
      </ul>
      <h2 class="text-xl mt-16 font-bold" id="m225">Bereitstellung des Onlineangebotes und Webhosting</h2>
      <p class="mt-4">
        Um unser Onlineangebot sicher und effizient bereitstellen zu können,
        nehmen wir die Leistungen von einem oder mehreren Webhosting-Anbietern
        in Anspruch, von deren Servern (bzw. von ihnen verwalteten Servern) das
        Onlineangebot abgerufen werden kann. Zu diesen Zwecken können wir
        Infrastruktur- und Plattformdienstleistungen, Rechenkapazität,
        Speicherplatz und Datenbankdienste sowie Sicherheitsleistungen und
        technische Wartungsleistungen in Anspruch nehmen.
      </p>
      <p class="mt-4">
        Zu den im Rahmen der Bereitstellung des Hostingangebotes verarbeiteten
        Daten können alle die Nutzer unseres Onlineangebotes betreffenden
        Angaben gehören, die im Rahmen der Nutzung und der Kommunikation
        anfallen. Hierzu gehören regelmäßig die IP-Adresse, die notwendig ist,
        um die Inhalte von Onlineangeboten an Browser ausliefern zu können, und
        alle innerhalb unseres Onlineangebotes oder von Webseiten getätigten
        Eingaben.
      </p>
      <p class="mt-4">
        <strong>Erhebung von Zugriffsdaten und Logfiles</strong>: Wir selbst
        (bzw. unser Webhostinganbieter) erheben Daten zu jedem Zugriff auf den
        Server (sogenannte Serverlogfiles). Zu den Serverlogfiles können die
        Adresse und Name der abgerufenen Webseiten und Dateien, Datum und
        Uhrzeit des Abrufs, übertragene Datenmengen, Meldung über erfolgreichen
        Abruf, Browsertyp nebst Version, das Betriebssystem des Nutzers,
        Referrer URL (die zuvor besuchte Seite) und im Regelfall IP-Adressen und
        der anfragende Provider gehören.
      </p>
      <p class="mt-4">
        Die Serverlogfiles können zum einen zu Zwecken der Sicherheit eingesetzt
        werden, z.B., um eine Überlastung der Server zu vermeiden (insbesondere
        im Fall von missbräuchlichen Angriffen, sogenannten DDoS-Attacken) und
        zum anderen, um die Auslastung der Server und ihre Stabilität
        sicherzustellen.
      </p>
      <p class="mt-4">
        <strong>Content-Delivery-Network</strong>: Wir setzen ein
        "Content-Delivery-Network" (CDN) ein. Ein CDN ist ein Dienst, mit dessen
        Hilfe Inhalte eines Onlineangebotes, insbesondere große Mediendateien,
        wie Grafiken oder Programm-Skripte, mit Hilfe regional verteilter und
        über das Internet verbundener Server schneller und sicherer ausgeliefert
        werden können.
      </p>
      <ul class="list-disc mt-4">
        <li>
          <p class="mt-4">
            <strong>Verarbeitete Datenarten:</strong> Inhaltsdaten (z.B.
            Texteingaben, Fotografien, Videos), Nutzungsdaten (z.B. besuchte
            Webseiten, Interesse an Inhalten, Zugriffszeiten),
            Meta-/Kommunikationsdaten (z.B. Geräte-Informationen, IP-Adressen).
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Betroffene Personen:</strong> Nutzer (z.B.
            Webseitenbesucher, Nutzer von Onlinediensten).
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Zwecke der Verarbeitung:</strong> Content Delivery Network
            (CDN), Vertragliche Leistungen und Service.
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Rechtsgrundlagen:</strong> Berechtigte Interessen (Art. 6
            Abs. 1 S. 1 lit. f. DSGVO).
          </p>
        </li>
      </ul>
      <p class="mt-4"><strong>Eingesetzte Dienste und Diensteanbieter:</strong></p>
      <ul class="list-disc mt-4">
        <li>
          <p class="mt-4">
            <strong>Netlify:</strong> Hostingplattform für Websites; Dienstanbieter:
            Netlify, Inc. Jurisdiction of Incorporation/Organization DELAWARE, CIK (Filer ID Number): 0001672598; 
            Netlify, Inc., 2325 3rd Street, Suite 215, 94107, San Francisco, California 
            Website:
            <a href="https://www.netlify.com" target="_blank">https://www.netlify.com</a
            >; Datenschutzerklärung:
            <a href="https://www.netlify.com/privacy/" target="_blank"
              >https://www.netlify.com/privacy/</a> 
            ; GDPR:
            <a href="https://www.netlify.com/gdpr/" target="_blank"
              >https://www.netlify.com/gdpr/</a> 
          </p>
        </li>
      </ul>
      <h2 class="text-xl mt-16 font-bold" id="m17">Newsletter und Breitenkommunikation</h2>
      <p class="mt-4">
        Wir versenden Newsletter, E-Mails und weitere elektronische
        Benachrichtigungen (nachfolgend "Newsletter“) nur mit der Einwilligung
        der Empfänger oder einer gesetzlichen Erlaubnis. Sofern im Rahmen einer
        Anmeldung zum Newsletter dessen Inhalte konkret umschrieben werden, sind
        sie für die Einwilligung der Nutzer maßgeblich. Im Übrigen enthalten
        unsere Newsletter Informationen zu unseren Leistungen und uns.
      </p>
      <p class="mt-4">
        Um sich zu unseren Newslettern anzumelden, reicht es grundsätzlich aus,
        wenn Sie Ihre E-Mail-Adresse angeben. Wir können Sie jedoch bitten,
        einen Namen, zwecks persönlicher Ansprache im Newsletter, oder weitere
        Angaben, sofern diese für die Zwecke des Newsletters erforderlich sind,
        zu tätigen.
      </p>
      <p class="mt-4">
        <strong>Double-Opt-In-Verfahren:</strong> Die Anmeldung zu unserem
        Newsletter erfolgt grundsätzlich in einem sogenannte
        Double-Opt-In-Verfahren. D.h., Sie erhalten nach der Anmeldung eine
        E-Mail, in der Sie um die Bestätigung Ihrer Anmeldung gebeten werden.
        Diese Bestätigung ist notwendig, damit sich niemand mit fremden
        E-Mail-Adressen anmelden kann. Die Anmeldungen zum Newsletter werden
        protokolliert, um den Anmeldeprozess entsprechend den rechtlichen
        Anforderungen nachweisen zu können. Hierzu gehört die Speicherung des
        Anmelde- und des Bestätigungszeitpunkts als auch der IP-Adresse. Ebenso
        werden die Änderungen Ihrer bei dem Versanddienstleister gespeicherten
        Daten protokolliert.
      </p>
      <p class="mt-4">
        <strong>Löschung und Einschränkung der Verarbeitung: </strong> Wir
        können die ausgetragenen E-Mail-Adressen bis zu drei Jahren auf
        Grundlage unserer berechtigten Interessen speichern, bevor wir sie
        löschen, um eine ehemals gegebene Einwilligung nachweisen zu können. Die
        Verarbeitung dieser Daten wird auf den Zweck einer möglichen Abwehr von
        Ansprüchen beschränkt. Ein individueller Löschungsantrag ist jederzeit
        möglich, sofern zugleich das ehemalige Bestehen einer Einwilligung
        bestätigt wird. Im Fall von Pflichten zur dauerhaften Beachtung von
        Widersprüchen behalten wir uns die Speicherung der E-Mail-Adresse
        alleine zu diesem Zweck in einer Sperrliste (sogenannte "Blacklist")
        vor.
      </p>
      <p class="mt-4">
        Die Protokollierung des Anmeldeverfahrens erfolgt auf Grundlage unserer
        berechtigten Interessen zu Zwecken des Nachweises seines ordnungsgemäßen
        Ablaufs. Soweit wir einen Dienstleister mit dem Versand von E-Mails
        beauftragen, erfolgt dies auf Grundlage unserer berechtigten Interessen
        an einem effizienten und sicheren Versandsystem.
      </p>
      <p class="mt-4">
        <strong>Hinweise zu Rechtsgrundlagen:</strong> Der Versand der
        Newsletter erfolgt auf Grundlage einer Einwilligung der Empfänger oder,
        falls eine Einwilligung nicht erforderlich ist, auf Grundlage unserer
        berechtigten Interessen am Direktmarketing, sofern und soweit diese
        gesetzlich, z.B. im Fall von Bestandskundenwerbung, erlaubt ist. Soweit
        wir einen Dienstleister mit dem Versand von E-Mails beauftragen,
        geschieht dies auf der Grundlage unserer berechtigten Interessen. Das
        Registrierungsverfahren wird auf der Grundlage unserer berechtigten
        Interessen aufgezeichnet, um nachzuweisen, dass es in Übereinstimmung
        mit dem Gesetz durchgeführt wurde.
      </p>
      <p class="mt-4">
        <strong>Inhalte</strong>: Informationen zu uns, unseren Leistungen,
        Aktionen und Angeboten.
      </p>
      <p class="mt-4">
        <strong>Erfolgsmessung</strong>: Die Newsletter enthalten einen
        sogenannte "web-beacon“, d.h., eine pixelgroße Datei, die beim Öffnen
        des Newsletters von unserem Server, bzw., sofern wir einen
        Versanddienstleister einsetzen, von dessen Server abgerufen wird. Im
        Rahmen dieses Abrufs werden zunächst technische Informationen, wie
        Informationen zum Browser und Ihrem System, als auch Ihre IP-Adresse und
        der Zeitpunkt des Abrufs, erhoben.
      </p>
      <p class="mt-4">
        Diese Informationen werden zur technischen Verbesserung unseres
        Newsletters anhand der technischen Daten oder der Zielgruppen und ihres
        Leseverhaltens auf Basis ihrer Abruforte (die mit Hilfe der IP-Adresse
        bestimmbar sind) oder der Zugriffszeiten genutzt. Diese Analyse
        beinhaltet ebenfalls die Feststellung, ob die Newsletter geöffnet
        werden, wann sie geöffnet werden und welche Links geklickt werden. Diese
        Informationen können aus technischen Gründen zwar den einzelnen
        Newsletterempfängern zugeordnet werden. Es ist jedoch weder unser
        Bestreben noch, sofern eingesetzt, das des Versanddienstleisters,
        einzelne Nutzer zu beobachten. Die Auswertungen dienen uns vielmehr
        dazu, die Lesegewohnheiten unserer Nutzer zu erkennen und unsere Inhalte
        an sie anzupassen oder unterschiedliche Inhalte entsprechend den
        Interessen unserer Nutzer zu versenden.
      </p>
      <p class="mt-4">
        Die Auswertung des Newsletters und die Erfolgsmessung erfolgen,
        vorbehaltlich einer ausdrücklichen Einwilligung der Nutzer, auf
        Grundlage unserer berechtigten Interessen zu Zwecken des Einsatzes eines
        nutzerfreundlichen sowie sicheren Newslettersystems, welches sowohl
        unseren geschäftlichen Interessen dient, als auch den Erwartungen der
        Nutzer entspricht.
      </p>
      <p class="mt-4">
        Ein getrennter Widerruf der Erfolgsmessung ist leider nicht möglich, in
        diesem Fall muss das gesamte Newsletterabonnement gekündigt, bzw. muss
        ihm widersprochen werden.
      </p>
      <p class="mt-4">
        <strong>Voraussetzung der Inanspruchnahme kostenloser Leistungen</strong
        >: Die Einwilligungen in den Versand von Mailings kann als Voraussetzung
        zur Inanspruchnahme kostenloser Leistungen (z.B. Zugang zu bestimmten
        Inhalten oder Teilnahme an bestimmten Aktionen) abhängig gemacht werden.
        Sofern die Nutzer die kostenlose Leistung in Anspruch nehmen möchten,
        ohne sich zum Newsletter anzumelden, bitten wir Sie um eine
        Kontaktaufnahme.
      </p>
      <ul class="list-disc mt-4">
        <li>
          <p class="mt-4">
            <strong>Verarbeitete Datenarten:</strong> Bestandsdaten (z.B. Namen,
            Adressen), Kontaktdaten (z.B. E-Mail, Telefonnummern),
            Meta-/Kommunikationsdaten (z.B. Geräte-Informationen, IP-Adressen),
            Nutzungsdaten (z.B. besuchte Webseiten, Interesse an Inhalten,
            Zugriffszeiten).
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Betroffene Personen:</strong> Kommunikationspartner, Nutzer
            (z.B. Webseitenbesucher, Nutzer von Onlinediensten).
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Zwecke der Verarbeitung:</strong> Direktmarketing (z.B. per
            E-Mail oder postalisch), Vertragliche Leistungen und Service.
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Rechtsgrundlagen:</strong> Einwilligung (Art. 6 Abs. 1 S. 1
            lit. a DSGVO), Berechtigte Interessen (Art. 6 Abs. 1 S. 1 lit. f.
            DSGVO).
          </p>
        </li>
        <li>
          <p class="mt-4">
            <strong>Widerspruchsmöglichkeit (Opt-Out):</strong> Sie können den
            Empfang unseres Newsletters jederzeit kündigen, d.h. Ihre
            Einwilligungen widerrufen, bzw. dem weiteren Empfang widersprechen.
            Einen Link zur Kündigung des Newsletters finden Sie entweder am Ende
            eines jeden Newsletters oder können sonst eine der oben angegebenen
            Kontaktmöglichkeiten, vorzugswürdig E-Mail, hierzu nutzen.
          </p>
        </li>
      </ul>
      <p class="mt-4"><strong>Eingesetzte Dienste und Diensteanbieter:</strong></p>
      <ul class="list-disc mt-4">
        <li>
          <p class="mt-4">
            <strong>Mailchimp:</strong> E-Mail-Marketing-Plattform;
            Dienstanbieter: "Mailchimp" - Rocket Science Group, LLC, 675 Ponce
            De Leon Ave NE #5000, Atlanta, GA 30308, USA; Website:
            <a href="https://mailchimp.com" target="_blank"
              >https://mailchimp.com</a
            >; Datenschutzerklärung:
            <a href="https://mailchimp.com/legal/privacy/" target="_blank"
              >https://mailchimp.com/legal/privacy/</a
            >; Privacy Shield (Gewährleistung Datenschutzniveau bei Verarbeitung
            von Daten in den USA):
            <a
              href="https://www.privacyshield.gov/participant?id=a2zt0000000TO6hAAG&status=Active"
              target="_blank"
              >https://www.privacyshield.gov/participant?id=a2zt0000000TO6hAAG&status=Active</a
            >.
          </p>
        </li>
      </ul>
      <h2 class="text-xl mt-16 font-bold" id="m12">Löschung von Daten</h2>
      <p class="mt-4">
        Die von uns verarbeiteten Daten werden nach Maßgabe der gesetzlichen
        Vorgaben gelöscht, sobald deren zur Verarbeitung erlaubten
        Einwilligungen widerrufen werden oder sonstige Erlaubnisse entfallen
        (z.B., wenn der Zweck der Verarbeitung dieser Daten entfallen ist oder
        sie für den Zweck nicht erforderlich sind).
      </p>
      <p class="mt-4">
        Sofern die Daten nicht gelöscht werden, weil sie für andere und
        gesetzlich zulässige Zwecke erforderlich sind, wird deren Verarbeitung
        auf diese Zwecke beschränkt. D.h., die Daten werden gesperrt und nicht
        für andere Zwecke verarbeitet. Das gilt z.B. für Daten, die aus handels-
        oder steuerrechtlichen Gründen aufbewahrt werden müssen oder deren
        Speicherung zur Geltendmachung, Ausübung oder Verteidigung von
        Rechtsansprüchen oder zum Schutz der Rechte einer anderen natürlichen
        oder juristischen Person erforderlich ist.
      </p>
      <p class="mt-4">
        Weitere Hinweise zu der Löschung von personenbezogenen Daten können
        ferner im Rahmen der einzelnen Datenschutzhinweise dieser
        Datenschutzerklärung erfolgen.
      </p>
      <ul class="list-disc mt-4"></ul>
      <h2 class="text-xl mt-16 font-bold" id="m15">Änderung und Aktualisierung der Datenschutzerklärung</h2>
      <p class="mt-4">
        Wir bitten Sie, sich regelmäßig über den Inhalt unserer
        Datenschutzerklärung zu informieren. Wir passen die Datenschutzerklärung
        an, sobald die Änderungen der von uns durchgeführten Datenverarbeitungen
        dies erforderlich machen. Wir informieren Sie, sobald durch die
        Änderungen eine Mitwirkungshandlung Ihrerseits (z.B. Einwilligung) oder
        eine sonstige individuelle Benachrichtigung erforderlich wird.
      </p>
      <p class="mt-4">
        Sofern wir in dieser Datenschutzerklärung Adressen und
        Kontaktinformationen von Unternehmen und Organisationen angeben, bitten
        wir zu beachten, dass die Adressen sich über die Zeit ändern können und
        bitten die Angaben vor Kontaktaufnahme zu prüfen.
      </p>
      <h2 class="text-xl mt-16 font-bold" id="m10">Rechte der betroffenen Personen</h2>
      <p class="mt-4">
        Ihnen stehen als Betroffene nach der DSGVO verschiedene Rechte zu, die
        sich insbesondere aus Art. 15 bis 18 und 21 DSGVO ergeben:
      </p>
      <ul class="list-disc mt-4">
        <li>
          <strong
            >Widerspruchsrecht: Sie haben das Recht, aus Gründen, die sich aus
            Ihrer besonderen Situation ergeben, jederzeit gegen die Verarbeitung
            der Sie betreffenden personenbezogenen Daten, die aufgrund von Art.
            6 Abs. 1 lit. e oder f DSGVO erfolgt, Widerspruch einzulegen; dies
            gilt auch für ein auf diese Bestimmungen gestütztes Profiling.
            Werden die Sie betreffenden personenbezogenen Daten verarbeitet, um
            Direktwerbung zu betreiben, haben Sie das Recht, jederzeit
            Widerspruch gegen die Verarbeitung der Sie betreffenden
            personenbezogenen Daten zum Zwecke derartiger Werbung einzulegen;
            dies gilt auch für das Profiling, soweit es mit solcher
            Direktwerbung in Verbindung steht.</strong
          >
        </li>
        <li>
          <strong>Widerrufsrecht bei Einwilligungen:</strong> Sie haben das
          Recht, erteilte Einwilligungen jederzeit zu widerrufen.
        </li>
        <li>
          <strong>Auskunftsrecht:</strong> Sie haben das Recht, eine Bestätigung
          darüber zu verlangen, ob betreffende Daten verarbeitet werden und auf
          Auskunft über diese Daten sowie auf weitere Informationen und Kopie
          der Daten entsprechend den gesetzlichen Vorgaben.
        </li>
        <li>
          <strong>Recht auf Berichtigung:</strong> Sie haben entsprechend den
          gesetzlichen Vorgaben das Recht, die Vervollständigung der Sie
          betreffenden Daten oder die Berichtigung der Sie betreffenden
          unrichtigen Daten zu verlangen.
        </li>
        <li>
          <strong
            >Recht auf Löschung und Einschränkung der Verarbeitung:</strong
          >
          Sie haben nach Maßgabe der gesetzlichen Vorgaben das Recht, zu
          verlangen, dass Sie betreffende Daten unverzüglich gelöscht werden,
          bzw. alternativ nach Maßgabe der gesetzlichen Vorgaben eine
          Einschränkung der Verarbeitung der Daten zu verlangen.
        </li>
        <li>
          <strong>Recht auf Datenübertragbarkeit:</strong> Sie haben das Recht,
          Sie betreffende Daten, die Sie uns bereitgestellt haben, nach Maßgabe
          der gesetzlichen Vorgaben in einem strukturierten, gängigen und
          maschinenlesbaren Format zu erhalten oder deren Übermittlung an einen
          anderen Verantwortlichen zu fordern.
        </li>
        <li>
          <strong>Beschwerde bei Aufsichtsbehörde:</strong> Sie haben ferner
          nach Maßgabe der gesetzlichen Vorgaben das Recht, bei einer
          Aufsichtsbehörde, insbesondere in dem Mitgliedstaat Ihres gewöhnlichen
          Aufenthaltsorts, Ihres Arbeitsplatzes oder des Orts des mutmaßlichen
          Verstoßes, wenn Sie der Ansicht sind, dass die Verarbeitung der Sie
          betreffenden personenbezogenen Daten gegen die DSGVO verstößt.
        </li>
      </ul>
      <h2 class="text-xl mt-16 font-bold" id="m42">Begriffsdefinitionen</h2>
      <p class="mt-4">
        In diesem Abschnitt erhalten Sie eine Übersicht über die in dieser
        Datenschutzerklärung verwendeten Begrifflichkeiten. Viele der Begriffe
        sind dem Gesetz entnommen und vor allem im Art. 4 DSGVO definiert. Die
        gesetzlichen Definitionen sind verbindlich. Die nachfolgenden
        Erläuterungen sollen dagegen vor allem dem Verständnis dienen. Die
        Begriffe sind alphabetisch sortiert.
      </p>
      <ul class="list-disc mt-4">
        <li>
          <strong>Content Delivery Network (CDN):</strong> Ein "Content Delivery
          Network" (CDN) ist ein Dienst, mit dessen Hilfe Inhalte eines
          Onlineangebotes, insbesondere große Mediendateien, wie Grafiken oder
          Programm-Skripte mit Hilfe regional verteilter und über das Internet
          verbundener Server, schneller und sicherer ausgeliefert werden können.
        </li>
        <li>
          <strong>Personenbezogene Daten:</strong> "Personenbezogene Daten“ sind
          alle Informationen, die sich auf eine identifizierte oder
          identifizierbare natürliche Person (im Folgenden "betroffene Person“)
          beziehen; als identifizierbar wird eine natürliche Person angesehen,
          die direkt oder indirekt, insbesondere mittels Zuordnung zu einer
          Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu
          einer Online-Kennung (z.B. Cookie) oder zu einem oder mehreren
          besonderen Merkmalen identifiziert werden kann, die Ausdruck der
          physischen, physiologischen, genetischen, psychischen,
          wirtschaftlichen, kulturellen oder sozialen Identität dieser
          natürlichen Person sind.
        </li>
        <li>
          <strong>Verantwortlicher:</strong> Als "Verantwortlicher“ wird die
          natürliche oder juristische Person, Behörde, Einrichtung oder andere
          Stelle, die allein oder gemeinsam mit anderen über die Zwecke und
          Mittel der Verarbeitung von personenbezogenen Daten entscheidet,
          bezeichnet.
        </li>
        <li>
          <strong>Verarbeitung:</strong> "Verarbeitung" ist jeder mit oder ohne
          Hilfe automatisierter Verfahren ausgeführte Vorgang oder jede solche
          Vorgangsreihe im Zusammenhang mit personenbezogenen Daten. Der Begriff
          reicht weit und umfasst praktisch jeden Umgang mit Daten, sei es das
          Erheben, das Auswerten, das Speichern, das Übermitteln oder das
          Löschen.
        </li>
      </ul>
      <p class="mt-4">
        <a
          href="https://datenschutz-generator.de/?l=de"
          title="Rechtstext von Dr. Schwenke - für weitere Informationen bitte anklicken."
          target="_blank"
          >Erstellt mit kostenlosem Datenschutz-Generator.de von Dr. Thomas
          Schwenke</a
        >
      </p>
    </div>



              
            </div>
            <!-- Eof: Datenschutz -->

          </div>
        </main>
      </div>
    </div>


  </Layout>
</template>