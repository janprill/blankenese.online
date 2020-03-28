<template>
  <Layout>
    <div x-data="{ open: false }" class="relative bg-white overflow-hidden">
      <div class="max-w-screen-xl mx-auto ">
        <div class="relative z-10 pb-8 bg-white sm:pb-16 md:pb-20 lg:max-w-2xl lg:w-full lg:pb-28 xl:pb-32">
          <div class="pt-6 px-4 sm:px-6 lg:px-8">
            <nav class="relative flex items-center justify-between sm:h-10 lg:justify-start">
              <div class="flex items-center flex-grow flex-shrink-0 lg:flex-grow-0">
                <div class="flex items-center justify-between w-full md:w-auto">
                  <a href="/">
                    <img class="h-8 w-auto sm:h-10" src="/img/logos/workflow-mark-on-white.svg" alt="" />
                  </a>
                  <div class="-mr-2 flex items-center md:hidden">
                    <button @click="open = true" type="button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500 transition duration-150 ease-in-out">
                      <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                      </svg>
                    </button>
                  </div>
                </div>
              </div>
              <div class="hidden md:block md:ml-10 md:pr-4">
                <a href="#" class="font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:text-gray-900 transition duration-150 ease-in-out">Kauf lokal!</a>
                <a href="#" class="ml-8 font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:text-gray-900 transition duration-150 ease-in-out">Helfen!</a>
                <a href="#" class="ml-8 font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:text-gray-900 transition duration-150 ease-in-out">Neuigkeiten</a>
                <a href="#" class="ml-8 font-medium text-gray-500 hover:text-gray-900 focus:outline-none focus:text-gray-900 transition duration-150 ease-in-out">Warum?</a>
              </div>
            </nav>
          </div>

          <div x-show="open" x-transition:enter="duration-150 ease-out" x-transition:enter-start="opacity-0 scale-95" x-transition:enter-end="opacity-100 scale-100" x-transition:leave="duration-100 ease-in" x-transition:leave-start="opacity-100 scale-100" x-transition:leave-end="opacity-0 scale-95" class="absolute top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden">
            <div class="rounded-lg shadow-md">
              <div class="rounded-lg bg-white shadow-xs overflow-hidden">
                <div class="px-5 pt-4 flex items-center justify-between">
                  <div>
                    <img class="h-8 w-auto" src="/img/logos/workflow-mark-on-white.svg" alt="" />
                  </div>
                  <div class="-mr-2">
                    <button @click="open = false" type="button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500 transition duration-150 ease-in-out">
                      <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                      </svg>
                    </button>
                  </div>
                </div>
                <div class="px-2 pt-2 pb-3">
                  <a href="#" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50 focus:outline-none focus:text-gray-900 focus:bg-gray-50 transition duration-150 ease-in-out">Kauf lokal!</a>
                  <a href="#" class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50 focus:outline-none focus:text-gray-900 focus:bg-gray-50 transition duration-150 ease-in-out">Helfen!</a>
                  <a href="#" class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50 focus:outline-none focus:text-gray-900 focus:bg-gray-50 transition duration-150 ease-in-out">Neuigkeiten</a>
                  <a href="#" class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50 focus:outline-none focus:text-gray-900 focus:bg-gray-50 transition duration-150 ease-in-out">Warum?</a>
                </div>
              </div>
            </div>
          </div>

          <div class="mt-10 mx-auto max-w-screen-xl px-4 sm:mt-12 sm:px-6 md:mt-16 lg:mt-20 lg:px-8 xl:mt-28">
            <div class="sm:text-center lg:text-left">
              <h2 class="text-4xl tracking-tight leading-10 font-extrabold text-gray-900 sm:text-5xl sm:leading-none md:text-6xl">
                Wir bringen Blankenese
                <br class="xl:hidden" />
                <span class="text-indigo-600">in der Krise online!</span>
              </h2>
              <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto md:mt-5 md:text-xl lg:mx-0">
                Hallo! Ich bin Jan Prill. Ich bin Entwicklungsleiter in einem mittelständischen Hamburger Unternehmen und ein Gewächs des Hamburger Westens. 
                Ich bin ausgewiesener eCommerce Profi und möchte Ihnen und Ihrem lokalen Unternehmen pro-bono, absolut kostenlos helfen, den Geschäftsbetrieb
                online aufrechtzuerhalten.
              </p>
              <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto md:mt-5 md:text-xl lg:mx-0">
                Alles was Sie tun müssen, ist meine kostenlose Hilfe anzunehmen. Was haben Sie zu verlieren? Legen wir los!
              </p>
              <div class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
                <div class="rounded-md shadow">
                  <a href="mailto:jan.prill@gmail.com" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base leading-6 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:shadow-outline transition duration-150 ease-in-out md:py-4 md:text-lg md:px-10">
                    Kontakt aufnehmen
                  </a>
                </div>
              </div>
            </div>
          </div>
          <svg class="hidden lg:block absolute right-0 inset-y-0 h-full w-48 text-white transform translate-x-1/2" fill="currentColor" viewBox="0 0 100 100" preserveAspectRatio="none">
            <polygon points="50,0 100,0 50,100 0,100" />
          </svg>
        </div>
      </div>
      <div class="lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2">
        <img class="h-56 w-full object-cover sm:h-72 md:h-96 lg:w-full lg:h-full" src="/img/blanke.jpg" alt="" />
      </div>
    </div>

    <!-- so funktioniert es -->
    <div class="py-12 bg-white">
      <div class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="mt-16">
          <p class="text-base leading-6 text-indigo-600 font-semibold tracking-wide uppercase">So helfe ich Ihnen. Kostenlos!</p>
          <h3 class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl sm:leading-10 max-w-2xl">
            Gemeinsam bringen wir Ihre Produkte online.
          </h3>
          <p class="mt-4 max-w-2xl text-xl leading-7 text-gray-500">
            Stellen Sie sich vor, alles was bislang im Dorf zu kaufen war, ist in der Krise online verfügbar. Wir alle, Nachbarn, Freunde,
            Blankeneser, Sülldorfer, Iserbrooker, Niendorfer halten in der Krise zusammen und unterstützen unsere lokalen Unternehmen.
          </p>
          <p class="mt-4 max-w-2xl text-xl leading-7 text-gray-500">
            Das geht! Das ist überhaupt kein Problem! Wenn es überhaupt etwas Gutes gibt, an der Coronakrise, dann gehört vielleicht folgende
            Erkenntnis dazu: Auch wenn Sie bisher nicht über den Onlineverkauf nachgedacht haben, sich vielleicht gelegentlich geradezu
            abgehängt gefühlt haben, von den großen Onlinehändlern: Jetzt ist der richtige Zeitpunkt, das zu ändern!
          </p> 
          <p class="mt-4 max-w-2xl text-xl leading-7 text-gray-500">
            Und so starten wir los:
          </p>
        </div>

        <div class="mt-10">
          <ul class="md:grid md:grid-cols-2 md:col-gap-8 md:row-gap-10">
            <li>
              <div class="flex">
                <div class="flex-shrink-0">
                  <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                    <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"/>
                    </svg>
                  </div>
                </div>
                <div class="ml-4">
                  <h5 class="text-lg leading-6 font-medium text-gray-900">Erster Schritt: wir nutzen einen kostenlosen Shop</h5>
                  <p class="mt-2 text-base leading-6 text-gray-500">
                    In der Krise überschlagen sich hervorragende Anbieter, wie ePages und Shopify mit Hilfsangeboten für kleine Unternehmen.
                    Es sind "no strings attached"! Sie bekommen einen kostenlosen Shop, mit dem Sie innerhalb der nächsten Stunden Ihre ersten
                    Verkäufe an Ihre Stammkunden, Nachbarn und Freunde machen können. Nur eben nicht mehr im Ladengeschäft, sondern online.
                  </p>
                </div>
              </div>
            </li>
            <li class="mt-10 md:mt-0">
              <div class="flex">
                <div class="flex-shrink-0">
                  <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                    <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 6l3 1m0 0l-3 9a5.002 5.002 0 006.001 0M6 7l3 9M6 7l6-2m6 2l3-1m-3 1l-3 9a5.002 5.002 0 006.001 0M18 7l3 9m-3-9l-6-2m0-2v2m0 16V5m0 16H9m3 0h3"/>
                    </svg>
                  </div>
                </div>
                <div class="ml-4">
                  <h5 class="text-lg leading-6 font-medium text-gray-900">Zweiter Schritt: Wir bauen einen Marktplatz</h5>
                  <p class="mt-2 text-base leading-6 text-gray-500">
                    Aus Ihrem Angebot, sowie den Angeboten Ihrer Kollegen aus dem lokalen Einzelhandel des Hamburger Westens bildet sich ein
                    Krisen-Marktplatz. Mehr und mehr Menschen werden online bestellen. Die Frage ist, ob sie dies so tun, dass Sie als lokaler
                    Anbieter weiter Geschäft machen, oder ob nur der Onlineversand profitiert. Lassen Sie uns den lokalen Markt stärken!s
                  </p>
                </div>
              </div>
            </li>
            <li class="mt-10 md:mt-0">
              <div class="flex">
                <div class="flex-shrink-0">
                  <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                    <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
                    </svg>
                  </div>
                </div>
                <div class="ml-4">
                  <h5 class="text-lg leading-6 font-medium text-gray-900">Dritter Schritt: Wir bauen ein lokalen "Versand" auf</h5>
                  <p class="mt-2 text-base leading-6 text-gray-500">
                    Sie selbst, Freunde, Verwandte, vielleicht Schüler bringen Waren direkt zum Kunden, der in der Nähe wohnt. 
                    Waren können abgeholt werden. Alles geschieht kontaktlos, weil die Ware bereits vorab per PayPal oder Kreditkarte
                    bezahlt wurde.
                  </p>
                </div>
              </div>
            </li>
            <li class="mt-10 md:mt-0">
              <div class="flex">
                <div class="flex-shrink-0">
                  <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                    <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"/>
                    </svg>
                  </div>
                </div>
                <div class="ml-4">
                  <h5 class="text-lg leading-6 font-medium text-gray-900">Vierter Schritt: Wenn die Krise vorbei ist</h5>
                  <p class="mt-2 text-base leading-6 text-gray-500">
                    Haben Sie Ihre ersten Schritte online gemacht und gehenn gestärkt aus dieser heftigen Situation hervor, die wir alle
                    gezwungenermaßen gerade miterleben. Sie werden das Beste aus der Situation gemacht haben.
                  </p>
                </div>
              </div>
            </li>
          </ul>
        </div>

        <div class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
          <div class="rounded-md shadow">
            <a href="mailto:jan.prill@gmail.com" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base leading-6 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:shadow-outline transition duration-150 ease-in-out md:py-4 md:text-lg md:px-10">
              Kontakt aufnehmen
            </a>
          </div>
        </div>


      </div>
    </div>
    <!-- eof: so funktioniert es -->





  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Blankenese online!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
