<template>
  <div>
    <ul v-for="(continent, index) in continents" :key="index">
      <li>{{ continent.name }}</li>
      <ul>
        <li v-for="(country, index) in continent.countries" :key="index">{{ country }}</li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Continents",
  data() {
    return {
      continents: [
        { 
          name: 'Europe', 
          countries: ['France', 'Germany', 'Spain', 'Italy', 'United Kingdom', 'Ukraine', 'Poland', 'Sweden'] 
        },
        { 
          name: 'Asia', 
          countries: ['China', 'India', 'Japan', 'Russia', 'Indonesia', 'Pakistan', 'Bangladesh', 'Thailand'] 
        },
        { 
          name: 'North America', 
          countries: ['United States', 'Canada', 'Mexico', 'Cuba', 'Jamaica', 'Haiti', 'Dominican Republic'] 
        },
        { 
          name: 'South America', 
          countries: ['Brazil', 'Argentina', 'Chile', 'Peru', 'Colombia', 'Venezuela', 'Ecuador'] 
        },
        { 
          name: 'Africa', 
          countries: ['Nigeria', 'Ethiopia', 'Egypt', 'South Africa', 'Kenya', 'Algeria', 'Morocco', 'Ghana'] 
        },
        { 
          name: 'Oceania', 
          countries: ['Australia', 'New Zealand', 'Fiji', 'Papua New Guinea', 'Samoa', 'Tonga', 'Vanuatu'] 
        }
      ]
    };
  }
};
</script>

<style>

</style>


