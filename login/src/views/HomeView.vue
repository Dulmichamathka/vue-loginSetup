<template>
  <v-app>
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row algin="center" justify="center">
          <v-col cols="12" sm="8" md="8">
            <v-card class="elevation-12">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 teal--text text--accent-3"
                        >
                          Sign into ShoppingStore
                        </h1>
                        <div class="text-center my-4" mt-4>
                          <v-btn class="mx-2 btn" fab color="black" outlined>
                            <v-icon>fab fa-facebook-f</v-icon>
                          </v-btn>
                          <v-btn class="mx-2 btn" fab color="black" outlined>
                            <v-icon>fab fa-google-plus-g</v-icon>
                          </v-btn>

                          <v-btn class="mx-2 btn" fab color="black" outlined>
                            <v-icon>fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mlt-4">
                          Ensure your email for registration
                        </h4>
                        <v-form>
                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="teal accent-3"
                          />

                          <v-text-field
                            id="password"
                            label="Password"
                            name="Password"
                            prepend-icon="lock"
                            type="password"
                            color="teal accent-3"
                          />
                        </v-form>

                        <h3 class="text-center mt-3">Forget Your Password?</h3>
                      </v-card-text>
                      <div class="text-center mt-2">
                        <v-btn class="mb-5" rounded color="teal accent-3" dark
                          >SIGN IN</v-btn
                        >
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="teal accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Hello, Friends !</h1>
                        <h5 class="text-center mx-10">
                          Enter your personnel details and start journey with us
                        </h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined="" dark @click="step++"
                          >SIGN UP</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row class="fill-height">
                    <v-col cols="12" md="4" class="teal accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Welcome Back !</h1>
                        <h5 class="text-center">
                          To Keep connected with us please login with your
                          personnel info
                        </h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined dark @click="step--"
                          >SIGN IN</v-btn
                        >
                      </div>
                    </v-col>
                    <v-col cols="12" md="8">
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 teal--text text--accent-3"
                        >
                          Create Account
                        </h1>
                        <div class="text-center mt-5">
                          <v-btn class="mx-2 btn" fab color="black" outlined>
                            <v-icon>fab fa-facebook-f</v-icon>
                          </v-btn>

                          <v-btn class="mx-2 btn" fab color="black" outlined>
                            <v-icon>fab fa-google-plus-g</v-icon>
                          </v-btn>

                          <v-btn class="mx-2 btn" fab color="black" outlined>
                            <v-icon>fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>

                        <h4 class="text-center mt-4">
                          Ensure your email for registration
                        </h4>

                        <v-form>
                          <v-text-field
                            label="Name"
                            name="Name"
                            prepend-icon="person"
                            type="text"
                            color="teal accent-3"
                          />

                          <v-text-field
                            label="Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="teal accent-3"
                          />

                          <v-text-field
                            label="Password"
                            name="Password"
                            prepend-icon="lock"
                            type="password"
                            color="teal accent-3"
                          />
                        </v-form>
                      </v-card-text>
                      <div class="text-center mt-n5">
                        <v-btn rounded color="teal accent-3" dark class="mb-5"
                          >SIGN UP</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
        </v-row>
        <router-view></router-view>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    step: 1,
  }),
  props: {
    source: String,
  },
};
</script>

<style>
.btn:hover {
  transition: transform 0.3s ease, background-color 0.3s ease;
  background-color: #64ffda; /* Example color for 'accent-3' */
  transform: scale(1.2); /* Increase size */
  border-color: white;
}

.btn {
  background-color: black;
  color: #64ffda;
}
.btn i {
  color: white !important;
}
</style>
