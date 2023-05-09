<template>
  <div>
    <v-row>
      <v-col>
        <h2 class="grey--text text--darken-2 text-center pb-4 text-uppercase">
          Minha Trajetório Profissional
        </h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-timeline>
          <v-timeline-item
            v-for="(company, index) in companiesWorked.reverse()"
            :key="company.name"
            :class="{ 'text-right': index % 2 == 1 }"
            color="grey darken-2"
          >
            <h3 class="pb-4 grey--text text--darken-2">{{ company.name }} ({{ company.period }})</h3>

            <v-expansion-panels>
              <v-expansion-panel v-for="role in company.roles" :key="role.name">
                <v-expansion-panel-header class="grey--text text--darken-2 font-weight-medium"> {{ role.name }} </v-expansion-panel-header>
                <v-expansion-panel-content> 
                    <div class="text-justify">
                        {{ role.description }}
                    </div>
                    <div class="d-flex flex-wrap">
                        <span class="mr-2 mt-3">Tecnologias:</span>
                        <v-chip class="mr-2 mt-2 white--text" color="blue darken-2" v-for="tecnology in role.technologies" :key="tecnology">
                            {{ tecnology }}
                        </v-chip>
                    </div> 
                </v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-timeline-item>
        </v-timeline>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      companiesWorked: [
        {
          name: "Softtek do Brasil",
          period: "2011 - 2016",
          roles: [
            { name: "Estágio de PMO", description: "Estágio de PMO" },
            {
              name: "Analista de Sistemas Trainee",
              description: "Analista de Sistemas Trainee",
            },
            {
              name: "Analista de Sistemas Junior",
              description: "Manutenção e implementação de novas funcionalidades em sistemas.",
              technologies: [".NET", "C#", "Delphi", "Javascript", "CSS", "Bootstrap", "HTML", "Oracle"]
            },
          ],
        },
        {
          name: "IMC",
          period: "2017 - 2019",
          roles: [
            {
              name: "Assistente de Controle e Gestão",
              description: "Assistente de C e G",
            },
          ],
        },
        {
          name: "Pirelli Pneus",
          period: "2019 - 2020",
          roles: [
            { name: "Estágio de Vendas", description: "Estágio de Vendas" },
          ],
        },
        {
          name: "CWS Digital",
          period: "2020 - Atualmente",
          roles: [
            {
              name: "Analista de Customer Growth",
              description: "Analista de Customer Growth",
            },
            { name: "Product Owner", description: "Product Owner" },
            {
              name: "Full Stack Developer",
              description: "Full Stack Developer",
            },
          ],
        },
      ],
      countCompanies: 4,
    };
  },
};
</script>

<style>
</style>