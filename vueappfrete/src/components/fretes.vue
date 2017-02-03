<template>
    <div>

        <div class="col-lg-3 filtros">
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
        <div class="col-lg-9 fretes" id="listafretes">
            <h5>Fretes {{ufo.length}}</h5>
            <div class="row">
            </div>
            <div class="row frete" v-for="frete in listaDeFretes" :key="frete.preco" v-if="frete.codorig == ufo || true">
                <div class="col-lg-10 dados-frete">
                    <div class="row">
                        <div class="col-lg-4">
                            <span>
                                Origem: <strong>{{ frete.origem }}</strong>
                            </span>
                            <span>
                                Destino: <strong>{{frete.destino}}</strong>
                            </span>
                        </div>
                        <div class="col-lg-4">
                            <span>
                                Produto: {{frete.produto}}
                            </span>
                            <span>
                                Espécie: {{frete.especie}}
                            </span>
                        </div>
                        <div class="col-lg-4">
                            <span>
                                Veículo: {{frete.veiculo}}
                            </span>
                            <span>
                                Preço: {{frete.preco}}
                            </span>
                        </div>
                    </div>
                </div>
                <div class="col-lg-2 logo-emp">
                </div>
                <div class="col-lg-12 frete-obs">
                    <div class="obs-texto">
                        {{frete.obs}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'tplfrete',
        data() {
            return {
                ufo: {},
                ufd: {},
                listaDeFretes: [
                { origem: 'Primavera do Leste / MT', codorig: 8,  destino: 'Imbituba / SC', produto: 'Soja', especie: 'Granel', veiculo: 'Rodotrem, Bitrem', preco: '195,00', obs: 'Há 1 min - Obs.: 150kg , 2 tampas.'},
                { origem: 'Ribeira do Amparo / BA', codorig: 1, destino: 'Campinas / SP', produto: 'Soja', especie: 'Granel', veiculo: 'Rodotrem, Bitrem', preco: '195,00', obs: 'Há 1 min - Obs.: 150kg , 2 tampas.' },
                { origem: 'Novo Hamburgo / RS', codorig: 9, destino: 'Arcos / MG', produto: 'Soja', especie: 'Granel', veiculo: 'Rodotrem, Bitrem', preco: '195,00', obs: 'Há 1 min - Obs.: 150kg , 2 tampas.' },
                { origem: 'Belo Horizonte / MG', codorig: 8, destino: 'Piçarras / SC', produto: 'Soja', especie: 'Granel', veiculo: 'Rodotrem, Bitrem', preco: '95,00', obs: 'Há 1 min - Obs.: 150kg , 2 tampas.' },
                { origem: 'Guarulhos / SP', codorig: 8, destino: 'Itaguaí / RJ', produto: 'Tanques', especie: 'Unidades', veiculo: 'Truck, Carreta', preco: '1905,00', obs: 'Há 1 min - Obs.: 150kg , 2 tampas.' },
                { origem: 'Pouso Alegre / MG', codorig: 8, destino: 'Cascavel / PR', produto: 'Gesso', especie: 'Paletes', veiculo: 'Rodotrem, Bitrem', preco: '200,00', obs: 'Há 1 min - KM: 489 - Obs.: livre de carga e descarga.' }
                ],
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

<style>
    .title-filtro{
        padding: 10px;
        background: #c2c2c2;
        text-align: center;
        font-size: 15px;
        margin-bottom: 20px;
        border-radius: 10px 10px 0px 0px;
    }
</style>

