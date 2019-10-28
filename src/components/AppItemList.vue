<template>
  <div>
    <h5>Prefixos <span class="badge badge-info"> {{prefixes.length}} </span> </h5>
            <div class="card">
              <div class="card-body">
                <ul class="list-group">
                  <li class="list-group-item" v-for="prefix in prefixes" v-bind:key="prefix">
										<div class="row">
											<div class="col-md">
												{{ prefix }}
											</div>
											<div class="col-md text-right">
												<button class="btn btn-info" v-on:click="deletePrefix(prefix)"><span class="fa fa-trash"></span></button>
											</div>
										</div>	
                  </li>
                </ul>
                <br>
                <div class="input-group">
                <input class="form-control" type="text" v-model="prefix" v-on:keyup.enter="addPrefix(prefix)" placeholder="Digite o Prefixo"/>
                <div class="input-group-append">
                  <button class="btn btn-info" v-on:click="addPrefix(prefix)"><span class="fa fa-plus"></span></button>
                </div>
                </div>
							</div>
            </div>
  </div>
</template>

<script>
export default {
	name: "AppItemList",
	props:["items"]
};

</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
