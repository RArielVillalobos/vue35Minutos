<template>
  <ul>
    <!-- con :key evitamos que devuelva elementos repetidos si los hubiera asi no arroja error , como el index es unico
     filtramos por ahi, hay que poner los : para decirq ue es una variable si ponemos el key sin los : decimos que se un atributo
     -->
    <li v-for="(user,index) in users" :key="index">
     {{index}} UserID: {{user.id}}, Email: {{user.email}}
    </li>
  </ul>

</template>

<script>
  export default {
    name:'users-list',
    data () {
      return {
        users:[
                {
                  "id": "5cb7a7c5c5b3e1911d1ddbe9",
                  "index": "5cb7a7c595ab0d526bab05e5",
                  "email": "5cb7a7c562e271cf9976f9b7",
                  "phone": "5cb7a7c5b0e6d05caa6f5ec5"
                },
                {
                  "id": "5cb7a7c5f9829f751c9d4046",
                  "index": "5cb7a7c574c1580ac8bd8ed0",
                  "email": "5cb7a7c51b34bbbe00db6a4e",
                  "phone": "5cb7a7c5cabf06fb45068548"
                },
                {
                  "id": "5cb7a7c55a59cb5b9628c3fa",
                  "index": "5cb7a7c5e6d5d13542d6808b",
                  "email": "5cb7a7c5595b20acd5e1a1a1",
                  "phone": "5cb7a7c51899f1001276fcab"
                },
                {
                  "id": "5cb7a7c56811fe5bf2efc9a2",
                  "index": "5cb7a7c5aa3864477a1ce61d",
                  "email": "5cb7a7c559b54beb8257c572",
                  "phone": "5cb7a7c50dd5afa2d8e206aa"
                },
                {
                  "id": "5cb7a7c505170e36f95db6ee",
                  "index": "5cb7a7c514f1d86004b84bee",
                  "email": "5cb7a7c51a3d018b9afba9c3",
                  "phone": "5cb7a7c5ead20071b138a391"
                },
                {
                  "id": "5cb7a7c5e71e67df8f309dec",
                  "index": "5cb7a7c554fc24b6a8a09f13",
                  "email": "5cb7a7c5c556b5d7af971aeb",
                  "phone": "5cb7a7c5ff7527477276be5a"
                },
                {
                  "id": "5cb7a7c57465df430adfc245",
                  "index": "5cb7a7c5a15131554b3172c2",
                  "email": "5cb7a7c567b55b610ead5db4",
                  "phone": "5cb7a7c5b38a879c889fff35"
                },
                {
                  "id": "5cb7a7c55bb6b03270d0f33b",
                  "index": "5cb7a7c59d4522ff935aed03",
                  "email": "5cb7a7c581b4755e04dad60f",
                  "phone": "5cb7a7c5bcf36b262323f98b"
                },
                {
                  "id": "5cb7a7c5a854bc956f632532",
                  "index": "5cb7a7c59583e0588bf0c522",
                  "email": "5cb7a7c55e1ff10e19f3ad63",
                  "phone": "5cb7a7c595bac280c9074af5"
                },
                {
                  "id": "5cb7a7c5921c7db3a9dc02fc",
                  "index": "5cb7a7c52390bbacff163f9d",
                  "email": "5cb7a7c5e2de117db49bd086",
                  "phone": "5cb7a7c55312553d3aa41bdd"
                },
                {
                  "id": "5cb7a7c5fe48d0a820e60130",
                  "index": "5cb7a7c5bab15ebf6216bc9a",
                  "email": "5cb7a7c58bb05fd36c496cb5",
                  "phone": "5cb7a7c5707d2e3894b49c9d"
                },
                {
                  "id": "5cb7a7c5d9dfca1f963fdfb3",
                  "index": "5cb7a7c578e579f2ca6af05f",
                  "email": "5cb7a7c5add101ac38903676",
                  "phone": "5cb7a7c508bf51e38eace810"
                },
                {
                  "id": "5cb7a7c5f26120876cd364ba",
                  "index": "5cb7a7c518f33bc459e58b26",
                  "email": "5cb7a7c52a20c5ee551b3806",
                  "phone": "5cb7a7c5b72af52aded5b24a"
                },
                {
                  "id": "5cb7a7c5f4e672ff922db595",
                  "index": "5cb7a7c5eb18cc1cbbadeccd",
                  "email": "5cb7a7c58039b5dfd9d55a1f",
                  "phone": "5cb7a7c51876dc6492f09aad"
                },
                {
                  "id": "5cb7a7c5e4507e74186c5e00",
                  "index": "5cb7a7c5693edd41f94540fe",
                  "email": "5cb7a7c55b99e283b64d4c64",
                  "phone": "5cb7a7c5128b339cea4f78df"
                },
                {
                  "id": "5cb7a7c5b835b85967086f3b",
                  "index": "5cb7a7c5364e5fabf15c2783",
                  "email": "5cb7a7c54c4d3a834db11669",
                  "phone": "5cb7a7c57b66fb62064f4e76"
                },
                {
                  "id": "5cb7a7c5fb17c549a5253718",
                  "index": "5cb7a7c503d799a40299415d",
                  "email": "5cb7a7c5cfa28da59898a51b",
                  "phone": "5cb7a7c57036272b25393b91"
                },
                {
                  "id": "5cb7a7c5516165e6c5ed62bd",
                  "index": "5cb7a7c51395bcf3e7ab829e",
                  "email": "5cb7a7c562487567779366e2",
                  "phone": "5cb7a7c500d57cb3173d749f"
                }
        ]

      }
    }

  }
</script>
