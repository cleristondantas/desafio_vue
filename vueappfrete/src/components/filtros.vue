<template>
  <div>
    <div class="row">
        <div class="col-lg-12 title-filtro">
            Filtrar Resultados
        </div>
    </div>

    <div class="row">
        <div class="col-lg-12">
            <div class="form-group">
                <label for="origem">Origem:</label>
                <select name="origem" id="origem" class="form-control" v-model="ufo">
                    <option v-for="option in options" v-bind:value="option.id">
                        {{ option.titulo }}
                    </option>
                </select>
            </div>
            <div class="form-group">
                <label for="destino">Destino:</label>
                <select name="destino" id="destino" class="form-control" v-model="ufd">
                    <option v-for="option in options" v-bind:value="option.id">
                        {{ option.titulo }}
                    </option>
                </select>
            </div>
        </div>
    </div>

  </div>
</template>

<script>

  export default{
    name : 'tplfiltro',
    data() {
            return {

                options: [
                    {
                        titulo: "Acre",
                        estado: "AC",
                        id: 1
                    },
                    {
                        titulo: "Mato Grosso",
                        estado: "MT",
                        id: 12
                    },
                    {
                        titulo: "Pará",
                        estado: "PA",
                        id: 13
                    },
                    {
                        titulo: "Paraíba",
                        estado: "PB",
                        id: 14
                    },
                    {
                        titulo: "Pernambuco",
                        estado: "PE",
                        id: 15
                    },
                    {
                        titulo: "Piauí",
                        estado: "PI",
                        id: 16
                    },
                    {
                        titulo: "Paraná",
                        estado: "PR",
                        id: 17
                    },
                    {
                        titulo: "Rio de Janeiro",
                        estado: "RJ",
                        id: 18
                    },
                    {
                        titulo: "Rio Grande do Norte",
                        estado: "RN",
                        id: 19
                    },
                    {
                        titulo: "Rondônia",
                        estado: "RO",
                        id: 20
                    },
                    {
                        titulo: "Roraima",
                        estado: "RR",
                        id: 21
                    },
                    {
                        titulo: "Rio Grande do Sul",
                        estado: "RS",
                        id: 22
                    },
                    {
                        titulo: "Santa Catarina",
                        estado: "SC",
                        id: 23
                    },
                    {
                        titulo: "Sergipe",
                        estado: "SE",
                        id: 24
                    },
                    {
                        titulo: "São Paulo",
                        estado: "SP",
                        id: 25
                    },
                    {
                        titulo: "Tocantins",
                        estado: "TO",
                        id: 26
                    },
                    {
                        titulo: "Mato Grosso do Sul",
                        estado: "MS",
                        id: 11
                    },
                    {
                        titulo: "Minas Gerais",
                        estado: "MG",
                        id: 10
                    },
                    {
                        titulo: "Maranhão",
                        estado: "MA",
                        id: 9
                    },
                    {
                        titulo: "Bahia",
                        estado: "BA",
                        id: 4
                    },
                    {
                        titulo: "Amapá",
                        estado: "AP",
                        id: 27
                    },
                    {
                        titulo: "Amazonas",
                        estado: "AM",
                        id: 3
                    },
                    {
                        titulo: "Distrito Federal",
                        estado: "DF",
                        id: 6
                    },
                    {
                        titulo: "Espírito Santo",
                        estado: "ES",
                        id: 7
                    },
                    {
                        titulo: "Alagoas",
                        estado: "AL",
                        id: 2
                    },
                    {
                        titulo: "Goiás",
                        estado: "GO",
                        id: 8
                    },
                    {
                        titulo: "Ceará",
                        estado: "CE",
                        id: 5
                    },
                    {
                        titulo: "Suriname",
                        estado: "SR",
                        id: 39
                    },
                    {
                        titulo: "Argentina",
                        estado: "AR",
                        id: 30
                    },
                    {
                        titulo: "Uruguai",
                        estado: "UY",
                        id: 28
                    },
                    {
                        titulo: "Bolívia",
                        estado: "BO",
                        id: 32
                    },
                    {
                        titulo: "Chile",
                        estado: "CL",
                        id: 35
                    },
                    {
                        titulo: "Colômbia",
                        estado: "CO",
                        id: 34
                    },
                    {
                        titulo: "Paraguai",
                        estado: "PY",
                        id: 29
                    },
                    {
                        titulo: "Perú",
                        estado: "PU",
                        id: 33
                    },
                    {
                        titulo: "Equador",
                        estado: "EQ",
                        id: 36
                    },
                    {
                        titulo: "Guiana Francesa",
                        estado: "GF",
                        id: 31
                    },
                    {
                        titulo: "Guiana Inglesa",
                        estado: "GY",
                        id: 38
                    },
                    {
                        titulo: "Venezuela",
                        estado: "VE",
                        id: 37
                    }
                ]
            }
        }
    }


</script>
