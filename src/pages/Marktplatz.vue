<template>
  <Layout>
    <div class="text-gray-600 font-copy text-lg container mx-auto">
      <h1 class="font-neuzeit text-4xl mt-16 font-bold">Marktplatz</h1>
      <div class="max-w-3xl">
        <p class="mt-6">
          Obwohl blankenese.online noch so eine junge Initiative ist, haben wir hier bereits einige Angebote und Dienstleistungen 
          versammelt. 
          Wir möchten Ihnen helfen, in der Krise besser klar zu kommen. Und Sie können selbst mit jeder Entscheidung als Verbraucher
          beeinflussen, wie Sie Einfluss auf die wirtschaftlichen Folgen der Krise nehmen. Und: Etwas Gutes kann das alles doch haben:
          Sie lernen hier Nachbarn kennen und erfahren von ihrer Arbeit, an denen Sie sonst einfach vorbeigelebt hätten.
        </p>
        <p class="mt-6">
          Wir zimmern das Schiff übrigens zusammen, während wir bereits lossegeln!
          Starten wir also mit dem Marktplatz:
        </p>
        <h2 class="mt-8 font-bold text-2xl">
          Gastronomie
        </h2>
        <Shop class="mt-10" url="background-image: url('/img/pizza.jpg')">
          <template v-slot:kicker>Pizza &amp; Pasta</template>
          <template v-slot:main>
            a modo nostro: Hausgemachte Pizza und Pasta
          </template>
          <template v-slot:bottom>
            Angelo und Lars von der Gastronomie an den Tennisplätzen des SVB sind für Euch da und ermöglichen telefonische Bestellungen. 
            Genießt Pizza, Pasta und Rustikales!
            <a class="underline" href="https://a-modo-nostro.blankenese.online" target="_blank">
              Hier geht es zu "a modo nostro". Aktuell noch gehostet auf blankenese.online, bald auf der eigenen Domain!
            </a>
          </template>
        </Shop>
        <h2 class="mt-8 font-bold text-2xl">
          Schönes / Geschenkideen von Blankeneser Unternehmen
        </h2>
        <Shop class="mt-10" url="background-image: url('/img/portrait_sina_large.jpg')">
          <template v-slot:kicker>design letters &amp; art prints</template>
          <template v-slot:main>
            Spoon: Fein typografierte und handgeschriebene Art Prints in hochwertiger Qualität und limitierter Auflage.
          </template>
          <template v-slot:bottom>Sina Peters bietet bei Ihrem Label Spoon fein typografierte und handgeschriebene Art Prints an, mit denen
            Sie Büro und Wohnung verschönern können. Schauen Sie sich in Ihrem Onlineshop um. Sina arbeitet aus ihrem Zuhause in Blankenese.
            <a class="underline" href="https://spoon-store.com/" target="_blank">
              Hier geht es zu Sinas Spoon-Store.
            </a>
          </template>
        </Shop>

        
        <h2 class="mt-8 font-bold text-2xl">
          Rechtsberatung
        </h2>
        <p class="mt-6">
          Anwaltliche Dienstleistungen können Sie telefonisch, oder per Videocall in Anspruch nehmen. Zwei Partner, bei denen sie 
          Hilfe bekommen können, wenn es z.B. Nachbarschaftsstreit gibt, oder die Krise bei Ihnen zu arbeitsrechtlichen Fragen führt.
        </p>
        <Shop class="mt-10" url="background-image: url('/img/dirk.jpg')">
          <template v-slot:kicker>Kostenlose Erstberatungen zu rechtlichen Fragen in der Krise</template>
          <template v-slot:main>
            Kanzlei Buggenthin &amp; Kollegen
          </template>
          <template v-slot:bottom>
            Auf meinen Post über blankenese.online hat sich RA Dirk Buggenthin direkt gemeldet und angeboten, in rechtlichen Fragen, die aus
            der Coronakrise entstehen eine kostenlose Erstberatung zu übernehmen. Dirk ist ein "Blankeneser Alumni"! Er war mit mir im gleichen
            Abijahrgang auf dem Gymnasium Blankense. Danke Dirk! 
            <a class="underline" href="https://www.kanzlei-buggenthin.de/" target="_blank">
              Zur Rechtsberatung bitte hier entlang.
            </a>
          </template>
        </Shop>
        <Shop class="mt-10" url="background-image: url('/img/MDL_Frontpage_Foto_1-4.jpg')">
          <template v-slot:kicker>Immobilienrecht / Nachbarrecht</template>
          <template v-slot:main>
            Rechtsanwalt De Luise
          </template>
          <template v-slot:bottom>
            Mit Kompetenz, Fachwissen und Erfahrung widmet sich Herr Rechtsanwalt De Luise den rechtlichen Angelegenheiten aus den Bereichen des Immobilienrechts und des Nachbarrechts.
            Auf blankense.online angesprochen fand er die Idee toll. Herr De Luise erarbeitet aktuell, ob er in der Krise Hausbesuche mit dem empfohlenen Mindestabstand anbieten kann und welche Alternativen es noch gibt.
            <a class="underline" href="http://rechtsanwalt-deluise.de/" target="_blank">
              Hier geht es zur Kanzleiseite von RA De Luise.
            </a>
          </template>
        </Shop>

        <h2 class="mt-8 font-bold text-2xl">
          Kultur
        </h2>
        <p class="mt-6">
          Nehmen Sie sich die Zeit, etwas Schönes zu lesen. Heymann, Ihr Buchladen am Blankeneser Bahnhof hat alle Bücher, die Sie sonst
          in der Krise wahrscheinlich bei Amazon bestellen würden.
        </p>
        <Shop class="mt-10" url="background-image: url('/img/silke.jpg')">
          <template v-slot:kicker>Silke Böschen</template>
          <template v-slot:main>
            Roman: Träume von Freiheit - Flammen am Meer
          </template>
          <template v-slot:bottom>
            Zum Programm, das Heymann liefern kann, gehört natürlich auch der Roman von unserer Blankeneser Nachbarin Silke Böschen: Zwei Frauen. Zwei Leben. Ein Drama.
            <a class="underline" href="https://www.gmeiner-verlag.de/buecher/titel/traeume-von-freiheit-flammen-am-meer.html" target="_blank">
              Auch als PDF und ePub beim Gmeiner Verlag bestellbar.
            </a>
          </template>
        </Shop>

        <h2 class="mt-8 font-bold text-2xl">
          Yoga / Coaching
        </h2>
        <p class="mt-6">
          Sport und Yoga kann macht auch in der Krise gemeinsam mehr Spaß. Das ist über Skype, Zoom, Hangouts möglich. 
        </p>
        <Shop class="mt-10" url="background-image: url('/img/danielaholm.jpg')">
          <template v-slot:kicker>Daniela Holm</template>
          <template v-slot:main>
            Yoga - Endlich aufblühen
          </template>
          <template v-slot:bottom>
            Daniela Holm bietet zum ersten Kennenlernen auf Ihrer toll gestalteten Internetseite ein kostenloses Telefongespräch von 20min an. Daniela unterstützt
            Sie in herausfordernden Lebensphasen unnd Krisen, zurück in Ihre Kraft und Leichtigkeit zu finden.
            <a class="underline" href="https://www.danielaholm.de/" target="_blank">
              Hier geht es zu Danielas Seite.
            </a>
          </template>
        </Shop>

        <h2 class="mt-8 font-bold text-2xl">
          Coaching
        </h2>
        <p class="mt-6">
          In der Krise kann es besonders helfen, mit jemandem zu sprechen, andere Perspektiven zu gewinnen.
        </p>
        <Shop class="mt-10" url="background-image: url('/img/kristinamohr.jpg')">
          <template v-slot:kicker>Kristina Mohr</template>
          <template v-slot:main>
            Trainings in Entspannung und Clownerie
          </template>
          <template v-slot:bottom>
            Kristina zeigt auf ihrer Website ihren Weg in der Krise. Ein Angebot für Entspannungs-Coaching und Clowns Coaching.
            <a class="underline" href="https://www.kristinamohr.de/" target="_blank">
              Hier geht es zu Kristinas Seite.
            </a>
          </template>
        </Shop>

        <p class="mt-6">
          Sie möchten auch hier gelistet werden? Dann nehmen Sie doch Kontakt auf...
        </p>
        <div class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
          <div class="rounded-md shadow">
            <a href="mailto:jan.prill@gmail.com" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base leading-6 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:shadow-outline transition duration-150 ease-in-out md:py-4 md:text-lg md:px-10">
              Kontakt aufnehmen
            </a>
          </div>
        </div>
        <p class="mt-6">
          Sie fragen sich, welche Unternehmen aus dem Hamburger Westen Sie aktuell unterstützen können? Sei es, weil sie bereits einen 
          Onlineshop haben, oder sei es, weil Sie ganz pragmatisch in der Krise eine telefonische Bestellung ermöglichen? Die beste Antwort
          gibt aktuell die 
          <a class="underline" href="https://www.blankenese-ig.de/" target="_blank">
            BLANKENESE Interessen Gemeinschaft e.V.
          </a>
        </p>
        <p class="mt-6">
          Und wir werden uns in den nächsten Tagen damit beschäftigen die Unternehmen pro-bono in den Onlinehandel zu bringen, die 
          bisher einen großen Bogen darum gemacht haben. Es ist an der Zeit.
        </p>
      </div>
    </div>
  </Layout>
</template>

<script>
import Shop from '~/components/Shop.vue'
export default {
  components: {
    Shop
  }
}
</script>