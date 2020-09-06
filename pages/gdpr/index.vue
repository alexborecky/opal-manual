<template>
  <div class="flex-row-hero">
    <aside class="col1">
      <contentList id="content-list"
          :introContent="page.introChapter"
          :contentOne="page.chapterOne"
          :contentTwo="page.chapterTwo"
          :contentThree="page.chapterThree"
          :contentFour="page.chapterFour"
          :contentFive="page.chapterFive"
          :contentSix="page.chapterSix"
        />
      </aside>
    <div class="col2">
        <div class="container">
            <textTutorial
                :sectionTitle="gdpr.title"
            />
            <div class="gdpr">
                    <h5>I. Základní ustanovení</h5>
                    <p>1. Správcem osobních údajů podle čl. 4 bod 7 nařízení Evropského parlamentu a Rady (EU) 2016/679 o ochraně fyzických osob v souvislosti se zpracováním osobních údajů a o volném pohybu těchto údajů (dále jen: „GDPR”) je techka s.r.o. IČ 07587813 se sídlem Bělehradská 858/23, Vinohrady, 120 00 Praha 2 (dále jen: „správce“).</p>
                    <p>2. Kontaktní údaje správce jsou</p>
                    <div class="wrapper">
                        <p>
                            adresa: Všechlapy 259, Nymburk 28802 <br>
                            email: info@tomashlad.eu <br>
                            telefon: +420 776 207 147‬
                        </p>
                    </div>
                    <p>
                        3. Osobními údaji se rozumí veškeré informace o identifikované nebo identifikovatelné fyzické osobě; identifikovatelnou fyzickou osobou je fyzická osoba, kterou lze přímo či nepřímo identifikovat, zejména odkazem na určitý identifikátor, například jméno, identifikační číslo, lokační údaje, síťový identifikátor nebo na jeden či více zvláštních prvků fyzické, fyziologické, genetické, psychické, ekonomické, kulturní nebo společenské identity této fyzické osoby.
                    </p>
                    <p>
                        4. Správce nejmenoval pověřence pro ochranu osobních údajů.
                    </p>
                    <h5>II. Zdroje a kategorie zpracovávaných osobních údajů</h5>
                    <p>
                        1. Správce zpracovává osobní údaje, které jste mu poskytl/a nebo osobní údaje, které správce získal na základě plnění Vaší objednávky.
                    </p>
                    <p>
                        2. Správce zpracovává Vaše identifikační a kontaktní údaje a údaje nezbytné pro plnění smlouvy.
                    </p>
                    <h5>III. Zákonný důvod a účel zpracování osobních údajů</h5>
                    <p>1. Zákonným důvodem zpracování osobních údajů je</p>
                    <div class="wrapper">
                        <ul>
                            <li><p>plnění smlouvy mezi Vámi a správcem podle čl. 6 odst. 1 písm. b) GDPR,</p></li>
                            <li><p>oprávněný zájem správce na poskytování přímého marketingu (zejména pro zasílání obchodních sdělení a newsletterů) podle čl. 6 odst. 1 písm. f) GDPR,</p></li>
                            <li><p>Váš souhlas se zpracováním pro účely poskytování přímého marketingu (zejména pro zasílání obchodních sdělení a newsletterů) podle čl. 6 odst. 1 písm. a) GDPR ve spojení s § 7 odst. 2 zákona č. 480/2004 Sb., o některých službách informační společnosti v případě, že nedošlo k objednávce zboží nebo služby. </p></li>
                        </ul>
                    </div>
                    <p>2. Účelem zpracování osobních údajů je</p>
                    <div class="wrapper">
                        <ul>
                            <li><p>vyřízení Vaší objednávky a výkon práv a povinností vyplývajících ze smluvního vztahu mezi Vámi a správcem; při objednávce jsou vyžadovány osobní údaje, které jsou nutné pro úspěšné vyřízení objednávky (jméno a adresa, kontakt), poskytnutí osobních údajů je nutným požadavkem pro uzavření a plnění smlouvy, bez poskytnutí osobních údajů není možné smlouvu uzavřít či jí ze strany správce plnit,</p></li>
                            <li><p>zasílání obchodních sdělení a činění dalších marketingových aktivit. </p></li>
                        </ul>
                    </div>
                    <p>
                        Ze strany správce nedochází k automatickému individuálnímu rozhodování ve smyslu čl. 22 GDPR. S takovým zpracováním jste poskytl/a svůj výslovný souhlas. 
                    </p>
                    <h5>IV. Doba uchovávání údajů</h5>
                    <p>1. Správce uchovává osobní údaje </p>
                    <div class="wrapper">
                        <ul>
                            <li><p>po dobu nezbytnou k výkonu práv a povinností vyplývajících ze smluvního vztahu mezi Vámi a správcem a uplatňování nároků z těchto smluvních vztahů (po dobu 15 let od ukončení smluvního vztahu). </p></li>
                            <li><p>po dobu, než je odvolán souhlas se zpracováním osobních údajů pro účely marketingu, nejdéle dvou let, jsou-li osobní údaje zpracovávány na základě souhlasu. </p></li>
                        </ul>
                    </div>
                    <p>2. Po uplynutí doby uchovávání osobních údajů správce osobní údaje vymaže. </p>
                    <h5>V. Příjemci osobních údajů (subdodavatelé správce)</h5>
                    <p>1. Příjemci osobních údajů jsou osoby </p>
                    <div class="wrapper">
                        <ul>
                            <li><p>podílející se na dodání zboží / služeb / realizaci plateb na základě smlouvy, </p></li>
                            <li><p>podílející se na zajištění provozu služeb,</p></li>
                            <li><p>zajišťující marketingové služby.</p></li>
                        </ul>
                    </div>
                    <p>2. Správce nemá v úmyslu předat osobní údaje do třetí země (do země mimo EU) nebo mezinárodní organizaci. Příjemci osobních údajů ve třetích zemích jsou poskytovatelé mailingových služeb / cloudových služeb.</p> 
                    <h5>VI. Vaše práva</h5>
                    <p>1. Za podmínek stanovených v GDPR máte </p>
                    <div class="wrapper">
                        <ul>
                            <li><p>právo na přístup ke svým osobním údajům dle čl. 15 GDPR,</p></li>
                            <p><li>právo opravu osobních údajů dle čl. 16 GDPR, popřípadě omezení zpracování dle čl. 18 GDPR.</li></p>
                            <li><p>právo na výmaz osobních údajů dle čl. 17 GDPR.</p></li>
                            <li><p>právo vznést námitku proti zpracování dle čl. 21 GDPR a </p></li>
                            <li><p>právo na přenositelnost údajů dle čl. 20 GDPR.</p></li>
                            <li><p>právo odvolat souhlas se zpracováním písemně nebo elektronicky na adresu nebo email správce uvedený v čl. III těchto podmínek. </p></li>
                        </ul>
                    </div>
                    <p>2. Dále máte právo podat stížnost u Úřadu pro ochranu osobních údajů v případě, že se domníváte, že bylo porušeno Vaší právo na ochranu osobních údajů.</p>
                    <h5>VII. Podmínky zabezpečení osobních údajů</h5>
                    <p>1. Správce prohlašuje, že přijal veškerá vhodná technická a organizační opatření k zabezpečení osobních údajů.</p>
                    <p>2. Správce přijal technická opatření k zabezpečení datových úložišť a úložišť osobních údajů v listinné podobě, zejména zabezpečená datová úložiště zajištěná bezpečnými hesly.</p>
                    <p>3. Správce prohlašuje, že k osobním údajům mají přístup pouze jím pověřené osoby.</p>

                    <h5>VIII. Závěrečná ustanovení</h5>
                    <p>1. Odesláním objednávky z internetového objednávkového formuláře potvrzujete, že jste seznámen/a s podmínkami ochrany osobních údajů a že je v celém rozsahu přijímáte.</p>
                    <p>2. S těmito podmínkami souhlasíte zaškrtnutím souhlasu prostřednictvím internetového formuláře. Zaškrtnutím souhlasu potvrzujete, že jste seznámen/a s podmínkami ochrany osobních údajů a že je v celém rozsahu přijímáte.</p>
                    <p>3. Správce je oprávněn tyto podmínky změnit. Novou verzi podmínek ochrany osobních údajů zveřejní na svých internetových stránkách, případně Vám zašle novou verzi těchto podmínek na e-mailovou adresu, kterou jste správci poskytl/a.</p>
                    <p>Tyto podmínky nabývají účinnosti dnem 25.5.2018.</p>
            </div>
        </div>
    </div>
  </div>
</template>
 
<script>
 
export default {
  async asyncData({$content}) {
    const page = await $content('home').fetch();
    const gdpr = await $content('gdpr').fetch();
    return {page, gdpr}
  },
  name: 'app',
  components: {
  },
  data () {
    return {
      name1: 'sectionTitle',
      chapterFour: 'sectionTitle',
      generatorTip: 'TIP! Vyzkoušejte náš generátor kódu pro bannery! Stačí vyplnit obsahová pole a kód máte pžipravený pro použiti.',
    }
  }
}
</script>

<style lang="scss">

p, h5 {
    margin-top: 32px !important;
}

.wrapper {
    padding-left: 24px;
    p {
        margin-top: 8px !important;
    }
}

</style>
