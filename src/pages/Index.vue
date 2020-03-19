<template>
  <Layout>
    <section class="container">
      <h2 class="text-xl flex items-center mb-10">
        <span>Is your library </span>
        <div class="relative ml-5">
          <select v-model="selected" class="block appearance-none w-full bg-gray-200 border border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-gray-500">
            <option v-for="library in libraries" :key="library" :value="library.value">
              {{ library.value }}
            </option>
          </select>
          <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
            <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"/></svg>
          </div>
        </div>
      </h2>
      
      <div v-if="selected === 'open'" class="flex flex-row flex-wrap">
        <div v-for="library in libraries[3].text" :key="library" class="self-center lg:w-1/5 px-6 py-4 mb-4 ml-4 text-center border rounded shadow">{{ library }}</div>
      </div>
      <div v-else-if="selected === 'open with reduced hours'" class="flex flex-row flex-wrap">
        <div v-for="library in libraries[2].text" :key="library" class="self-center lg:w-1/5 px-6 py-4 mb-4 ml-4 text-center border rounded shadow">{{ library }}</div>
      </div>
      <div v-else-if="selected === 'open with id only'" class="flex flex-row flex-wrap">
        <div v-for="library in libraries[1].text" :key="library" class="self-center lg:w-1/5 px-6 py-4 mb-4 ml-4 text-center border rounded shadow">{{ library }}</div>
      </div>
      <div v-else class="flex flex-row flex-wrap">
        <div v-for="library in libraries[0].text" :key="library" class="self-center lg:w-1/5 px-6 py-4 mb-4 ml-4 text-center border rounded shadow">{{ library }}</div>
      </div>

    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Home"
  },
  data() {
    return {
      selected: 'open',
      libraries: [
        {
          value: "closed",
          text: ["Auburn University","Bibliothèque de l'Université Laval","Boston College","Boston Public Library","Boston University","Brown University (Annex pending)","Case Western Reserve","Center for Research Libraries","Columbia University","Cornell University","Dartmouth College","Duke University","Harvard University","Howard University","Johns Hopkins University","Kent State University","Library of Congress","Louisiana State University","McGill University","McMaster University","Michigan State University","MIT","National Agricultural Library","National Archives","New York Public Library","New York University","Northwestern University","Ohio State University","Princeton University","Rice University","Rutgers University","Smithsonian Libraries","Syracuse University","Temple University (after March 19)","Tulane University","UC Berkeley","UC Irvine","UC Los Angeles (after March 19)","UC Riverside","UC San Diego","UC Santa Barbara (after March 19)","University of Alabama","University of Arizona","University of Cincinnati","University of Colorado, Boulder","University of Connecticut","University of Delaware","University of Georgia","University of Iowa","University of Kansas","University of Kentucky","University of Maryland","University of Miami","University of Michigan","University of Minnesota","University of Missouri","University of New Mexico","University of North Carolina","University of Oklahoma","University of Ottawa","University of Pennsylvania (Penn)","University of Pittsburgh (Pitt)","University of Rochester","University of South Carolina","University of Southern California","University of Tennessee, Knoxville","University of Virginia","University of Washington","University of Waterloo","University of Wisconsin-Madison","Washington University in St. Louis","Wayne State University","Western University","Yale University","York University"]
        },
        {
          value: "open with id only",
          text: ["Colorado State University","Emory University","Florida State University","George Washington University (until 3/20)","Indiana University Bloomington","North Carolina State University","Ohio University (until 3/20)","University of Alberta","University of Calgary","University of Guelph","University of Hawaii at Manoa","University of Notre Dame","University of Oregon","University of Utah","Vanderbilt University"]
        },
        {
          value: "open with reduced hours",
          text: ["Arizona State University","Brigham Young University","Emory University","Georgetown University","Georgia Institute of Technology","Iowa State University","Oklahoma State University","Penn State University","Purdue University (until 3/20)","Queen's University","Simon Fraser University (will close 3/21)","Stony Brook University (SUNY)","Texas A&M University","Texas Tech University","UC Davis","University at Albany (SUNY)","University of British Columbia","University at Buffalo (SUNY) (one branch)","University of Florida","University of Illinois at Chicago","University of Illinois at Urbana-Champaign","University of Kansas","University of Louisville","University of Manitoba","University of Massachusetts Amherst","University of Nebraska-Lincoln (one branch)","University of Saskatchewan (will close 3/20)","University of Texas at Austin","University of Toronto","Virginia Commonwealth University (will close 3/20)","Virginia Tech","Washington State University"]
        },
        {
          value: "open",
          text: ["Southern Illinois University, Carbondale","University of Chicago (will close 3/20)"]
        }
      ]
    }
  }
};
</script>
