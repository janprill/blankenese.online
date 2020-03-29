<template>
  <Layout>
    <div class="text-gray-600 font-copy text-lg container mx-auto">
      <h1 class="font-neuzeit text-4xl mt-16 font-bold">Marktplatz</h1>
      <div class="max-w-3xl">
        <p class="mt-6">
          Obwohl blankenese.online noch so eine junge Initiative ist, haben wir hier bereits einige Angebote und Dienstleistungen 
          versammelt, die Ihnen helfen können, in der Krise besser klar zu kommen und mit denen Sie helfen können, dass Unternehmen 
          oder Einzelpersonen aus Ihrer unmittelbaren Nachbarschaft in dieser herausfordernden Zeit wirtschaftlichen Erfolg haben.
        </p>
        <p class="mt-6">
          Wir zimmern das Schiff zusammen, während wir schon los segeln!
          Starten wir also mit dem unserem Marktplatz:
        </p>
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
          </template>
        </Shop>

        
        <h2 class="mt-8 font-bold text-2xl">
          Rechtsberatung
        </h2>
        <p class="mt-6">
          Anwaltliche Dienstleistungen können Sie telefonisch, oder per Videocall in Anspruch nehmen. Zwei Partner, bei denen sie 
          Hilfe bekommen können, wenn es z.B. Nachbarschaftsstreit gibt, oder die Krise bei Ihnen zu arbeitsrechtlichen Fragen führt.
        </p>
        <Shop class="mt-10" url="background-image: url('/img/portrait_sina_large.jpg')">
          <template v-slot:kicker>Kostenlose Erstberatungen zu rechtlichen Fragen in der Krise</template>
          <template v-slot:main>
            Kanzlei Buggenthin &amp; Kollegen
          </template>
          <template v-slot:bottom>
            Auf meinen Post über blankenese.online hat sich RA Dirk Buggenthin direkt gemeldet und angeboten, in rechtlichen Fragen, die aus
            der Coronakrise entstehen eine kostenlose Erstberatung zu übernehmen. Dirk ist ein "Blankeneser Alumni"! Er war mit mir im gleichen
            Abijahrgang auf dem Gymnasium Blankense. Danke Dirk!s
          </template>
        </Shop>
        <Shop class="mt-10" url="background-image: url('/img/portrait_sina_large.jpg')">
          <template v-slot:kicker>Immobilienrecht / Nachbarrecht</template>
          <template v-slot:main>
            
          </template>
          <template v-slot:bottom>
            Auf meinen Post über blankenese.online hat sich RA Dirk Buggenthin direkt gemeldet und angeboten, in rechtlichen Fragen, die aus
            der Coronakrise entstehen eine kostenlose Erstberatung zu übernehmen. Dirk ist ein "Blankeneser Alumni"! Er war mit mir im gleichen
            Abijahrgang auf dem Gymnasium Blankense. Danke Dirk!s
          </template>
        </Shop>

        <h2 class="mt-8 font-bold text-2xl">
          Kultur
        </h2>
        <p class="mt-6">
          Nehmen Sie sich die Zeit, etwas Schönes zu lesen. Heymann, Ihr Buchladen am Blankeneser Bahnhof bestellt alle Bücher, die Sie sonst
          bei geschlossenen Geschäften wahrscheinlich bei Amazon bestellen würden.
        </p>

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