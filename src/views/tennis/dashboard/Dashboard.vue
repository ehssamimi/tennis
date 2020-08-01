<template>
  <div>
    <!-- Hero -->

    <!-- END Hero -->

    <!-- Page Content -->
    <div class="content  p-0">

      <b-row class="row-deck">

        <!-- Fields   -->
        <b-col lg="8">
          <base-block title="مدیریت زمین ها  " dir="rtl" :bLine="false"  class="Fs4 text-right br-box-t p-0   position-relative " content-full>
            <b-row>
              <b-col sm="8" class="position-relative row">

                <b-col sm="6" class="position-relative row">
                  <b-col sm="12" class="position-relative  m-0 d-flex flex-column justify-content-around h-100">
                    <div class="w-100 position-relative br-box-img" @click="form=!form">
                      <div class="position-absolute w-100  pr-4 mt-3  " >
                        <HeaderBoxField :types="`red-btn`" :numberField="3"/>
                        <p class="  text-white Fs0-3 mt-4 mb-0 text-center"   >زمین آزاد است</p>
                      </div>
                      <b-img src="img/S-img/bg-light.png" class=" w-100 " />
                    </div>
                    <div class="w-100 position-relative">
                      <div class="position-absolute w-100  pr-4 mt-3 " >
                        <HeaderBoxField :types="`green-btn`" :numberField="4"/>
                        <p class="  text-white Fs0-3 mt-4 mb-0 text-center"   >زمین غیر فعال است</p>
                      </div>
                      <b-img src="img/S-img/bg-black.png" class="w-100  br-box-img " />
                    </div>
                  </b-col>
                </b-col>
                <b-col sm="6" class="position-relative   h-100">
                  <b-col sm="12" class="position-relative  m-0 d-flex flex-column justify-content-around h-100">
                    <div class="w-100 position-relative">
                      <div class="position-absolute w-100  pr-4  mt-3" >
                        <HeaderBoxField :types="`green-btn`" :numberField="1"/>
                        <div class="mt-3">
                          <BoxNameCountDown :number="2" :name="`کیوان یعقوبیان`"/>

                        </div>

                      </div>
                      <b-img src="img/S-img/bg-black.png" class="w-100 br-box-img" />
                    </div>
                    <div class="w-100 position-relative">
                      <div class="position-absolute w-100  pr-4 mt-3  " >
                        <HeaderBoxField :types="`green-btn`" :numberField="2"/>
                        <div class="mt-3">
                        <BoxNameCountDown :number="1" :name="`مهدی فلاحتی`"/>
                        </div>
                      </div>
                      <b-img src="img/S-img/bg-black.png" class="w-100 br-box-img" />
                    </div>
                  </b-col>
                </b-col>


              </b-col>
              <b-col sm="4">


                <div class="w-100 position-relative  ">
                  <div  v-if="form"  class="w-100 position-absolute h-100 p-3">
                    <div class="w-100 border-b-s">
                      <h4 class="block-title pb-3 Fs0-3 ">
                        زمین شماره سه
                      </h4>
                    </div>
                    <div class="w-100 border-b-s ">
                      <p class="Fs0-1">فعال/غیر فعال سازی تمام زمین ها </p>
                      <b-col cols="6" class="p-0" >
                        <b-form-group label="تاریخ  " label-for="data-field" class="Fs0-1 mb-1">
                          <b-form-input id="data-field"   class="b-input-box   outline-none " size="sm" ></b-form-input>
                        </b-form-group>
                      </b-col>
                      <b-col cols="12 " class="p-0" >
                        <b-form-group label="بازه زمانی  " label-for="data-interval" class="Fs0-1 mb-1">
                          <div class="w-100 d-flex ">
                            <b-col cols="4   " class="pr-0" >
                              <b-form-group label-cols-sm="3" label="از" label-for="from" class="mb-1">
                                <b-form-input id="from"   class="b-input-box   outline-none " size="sm" ></b-form-input>
                              </b-form-group>
                            </b-col>
                            <b-col cols="4 " class="pr-0" >
                              <b-form-group label-cols-sm="3" label="تا" label-for="to" class="mb-1">
                                <b-form-input id="to"   class="b-input-box outline-none " size="sm" ></b-form-input>
                              </b-form-group>
                            </b-col>
                            <b-col cols="4  " class="pr-0 pl-0 cursor-pointer">
                              <b-form-group label="" label-for="data-field" class="Fs0-1 mb-1 cursor-pointer">
                                <div class="Bg-submit br-round d-flex align-items-center p-05   justify-content-center ">
                                  <p class="Fs0-2 text-white mb-0 text-nowrap">فعال کردن</p>
                                </div>
                              </b-form-group>
                            </b-col>
                          </div>
                         </b-form-group>
                      </b-col>


                    </div>
                    <div class="w-100  mt-2 ">
                      <p class="Fs0-1 mb-0">رزرو دستی </p>
                      <b-col cols="8" class="p-0" >
                        <b-form-group label="نام نام خانوادگی بازیکن " label-for="data-field" class="Fs0-1 mb-1">
                          <b-form-input id="data-field"   class="b-input-box   " size="sm" ></b-form-input>
                        </b-form-group>
                      </b-col>
                      <b-col cols="12 " class="p-0" >
                        <b-form-group label=" " label-for="data-interval" class="Fs0-1">
                          <div class="w-100 d-flex ">
                            <b-col cols="4   " class="pr-0" >
                              <b-form-group label="ساعت شروع  " label-for="data-field" class="Fs0-1 mb-1">
                                <b-form-input id="data-field"   class="b-input-box    " size="sm" ></b-form-input>
                              </b-form-group>
                            </b-col>
                            <b-col cols="4 " class="pr-0" >
                              <b-form-group label="تعداد سانس " label-for="data-field" class="Fs0-1 mb-1">
                                <div class="w-100 d-flex form-control form-control-sm   br-round ">
                               <b-col cols="3" class="p-0 cursor-pointer " @click="number=number+1"> <i  class="fa   fa-plus"></i></b-col>
                               <b-col cols="6" class="d-flex justify-content-center">{{number}}</b-col>
                               <b-col cols="3" class="p-0 cursor-pointer"  @click="number=number-1"><i  class=" fa   fa-minus"></i></b-col>

                                </div>
                               </b-form-group>
                            </b-col>
                            <b-col cols="4  " class="pr-0 pl-0">
                              <b-form-group label=" ` " label-for="data-field" class="Fs0-1 mb-1 cursor-pointer">
                                <div class="Bg-submit br-round d-flex align-items-center p-05   justify-content-center ">
                                  <p class="Fs0-2 text-white mb-0 text-nowrap">فعال کردن</p>
                                </div>
                              </b-form-group>

                            </b-col>
                          </div>
                        </b-form-group>
                      </b-col>


                    </div>
                  </div>
                  <div v-else class="w-100 position-absolute h-100 p-3">
                    <div class="w-100  ">
                      <h4 class="block-title pb-3 Fs0-3 ">
                       کل زمین ها
                      </h4>
                      <div class="d-flex flex-column border-b-s pb-3">
                        <div class="d-flex align-items-center">
                          <span class="circle c-green"></span>
                          <span class="Fs0-1 mr-2">زمین های فعال </span>
                          <span class="Fs0-1 mr-auto">3</span>
                        </div>
                        <div class="d-flex align-items-center">
                          <span class="circle c-orange"></span>
                          <span class="Fs0-1 mr-2">زمین های آزاد </span>
                          <span class="Fs0-1 mr-auto">1</span>
                        </div>
                        <div class="d-flex align-items-center">
                          <span class="circle c-white"></span>
                          <span class="Fs0-1 mr-2">زمین های غیر فعال </span>
                          <span class="Fs0-1 mr-auto">1</span>
                        </div>
                      </div>
                    </div>
                    <div class="w-100 border-b-s pt-3">
                      <p class="Fs0-1">فعال/غیر فعال سازی تمام زمین ها </p>
                      <b-col cols="6" class="p-0" >
                        <b-form-group label="تاریخ  " label-for="data-field" class="Fs0-1 mb-1">
                          <b-form-input id="data-field"   class="b-input-box   outline-none " size="sm" ></b-form-input>
                        </b-form-group>
                      </b-col>
                      <b-col cols="12 " class="p-0" >
                        <b-form-group label="بازه زمانی  " label-for="data-interval" class="Fs0-1 mb-1">
                          <div class="w-100 d-flex ">
                            <b-col cols="4   " class="pr-0" >
                              <b-form-group label-cols-sm="3" label="از" label-for="from"  class="Fs0-1 mb-1">
                                <b-form-input id="from"   class="b-input-box   outline-none " size="sm" ></b-form-input>
                              </b-form-group>
                            </b-col>
                            <b-col cols="4 " class="pr-0" >
                              <b-form-group label-cols-sm="3" label="تا" label-for="to"  class="Fs0-1 mb-1">
                                <b-form-input id="to"   class="b-input-box outline-none " size="sm" ></b-form-input>
                              </b-form-group>
                            </b-col>
                            <b-col cols="4  " class="pr-0 pl-0 cursor-pointer">
                              <b-form-group label="" label-for="data-field" class="Fs0-1 mb-1 cursor-pointer">
                                <div class="Bg-submit br-round d-flex align-items-center p-05   justify-content-center ">
                                  <p class="Fs0-2 text-white mb-0 text-nowrap">فعال کردن</p>
                                </div>
                              </b-form-group>
                            </b-col>
                          </div>
                        </b-form-group>
                      </b-col>


                    </div>
                    <div class="w-100   pt-3 ">
                      <p class="Fs0-1 mb-0">تغییر زمان کاری  </p>
                      <div class="w-100 d-flex ">
                        <b-col cols="4   " class="pr-0" >
                          <b-form-group label-cols-sm="3" label="از" label-for="from" class="mb-1">
                            <b-form-input id="from"   class="b-input-box   outline-none " size="sm" ></b-form-input>
                          </b-form-group>
                        </b-col>
                        <b-col cols="4 " class="pr-0" >
                          <b-form-group label-cols-sm="3" label="تا" label-for="to" class="mb-1">
                            <b-form-input id="to"   class="b-input-box outline-none " size="sm" ></b-form-input>
                          </b-form-group>
                        </b-col>
                        <b-col cols="4  " class="pr-0 pl-0 cursor-pointer">
                          <b-form-group label="" label-for="data-field" class="Fs0-1 mb-1 cursor-pointer">
                            <div class="Bg-submit br-round d-flex align-items-center p-05   justify-content-center ">
                              <p class="Fs0-2 text-white mb-0 text-nowrap">فعال کردن</p>
                            </div>
                          </b-form-group>
                        </b-col>
                      </div>


                    </div>
                  </div>


                </div>

                <b-img src="img/S-img/b-form.png" class="w-100" />
              </b-col>
            </b-row>

          </base-block>
        </b-col>
        <!-- END Fields -->

        <!-- Latest Customers -->
        <b-col xl="4" dir="rtl"  >
          <base-block title="لیست رزروها " dir="rtl"  class="Fs4 text-right br-box-t p-0   position-relative "  :bLine="true" content-full>
            <div class="d-flex flex-column ">
              <b-table-simple   hover borderless class="table-vcenter font-size-sm mb-0 position-relative   ">
                <!--              <div class="border-t-s"></div>-->
                <b-thead  >
                  <b-tr>
                    <b-th class="d-none d-sm-table-cell font-w600 text-center Fs1" style=" "> </b-th>
                    <b-th class="font-w600 Fs0-1 text-right text-nowrap pr-0" style=" ">نام و نام خانوادگی </b-th>
                    <b-th class="  font-w600 text-center Fs0-1  pr-0 pl-0" style="width: 30px "  >تاریخ </b-th>
                    <b-th class="  font-w600 text-center Fs0-1 text-nowrap pr-0" style="width: 30px "  >ساعت رزرو </b-th>
                    <b-th class="  font-w600 text-center   Fs0-1 text-nowrap pr-0 pl-0" style="width: 30px "  >ساعت پایان   </b-th>


                  </b-tr>
                </b-thead>
                <b-tbody class="position-relative">


                  <b-tr v-for="(customer, index) in latestCustomers"   :key="index"   :class = "(index===0)?' ':'border-t-s'" >

                    <b-td class="d-none d-sm-table-cell text-right pr-0">
                      <img class="img-avatar img-avatar-vw" :src="`img/avatars/${customer.avatar}.jpg`" alt="Avatar">
                    </b-td>
                    <b-td class="text-right pr-0">
                      <span  class="  font-w600 Fs1" href="javascript:void(0)">{{ customer.name }}</span>
                    </b-td>
                    <b-td class=" text-center" style="width: 30px " >
                      <span  class="link-fx font-w600 Fs1" href="javascript:void(0)">{{ customer.orders }}</span>
                    </b-td>
                    <b-td class="  text-center" style="width: 30px " >
                      <span  class="link-fx font-w600 Fs1" href="javascript:void(0)">{{ customer.orders }}</span>
                    </b-td>
                    <b-td class="  text-center" style="width: 30px " >
                      <span  class="link-fx font-w600 Fs1" href="javascript:void(0)">{{ customer.orders }}</span>
                    </b-td>
                  </b-tr>

                </b-tbody>


              </b-table-simple>
              <div class="زخم-6 ">
                <div class="position-absolute" style="bottom: 2vw; left: 2vw">
                  <div class="Bg-submit br-round d-flex align-items-center p-05 mt-3 justify-content-center pr-4 pl-4 ">
                    <p class="Fs0-2 text-white mb-0 text-nowrap">مشاهده همه</p>
                  </div>
                </div>

                <b-img src="img/S-img/Rectangle 23.png" class="opacity-0"/>
              </div>

            </div>

          </base-block>
        </b-col>
        <!-- END Latest Customers -->



        <!-- Latest Customers -->
        <b-col xl="5" dir="rtl"  >
          <base-block  dir="rtl"  class="Fs4 text-right br-box-t p-0   position-relative " content-full>
            <b-row name="header"  >
              <b-col sm="6">
                <h3 class="block-title pb-3 ">
                  اعلان ها
                </h3>
              </b-col>

              <b-col sm="5" class="block-options classContainerOptions br-round d-flex align-items-center mr-auto  "  >
                <div :class = "notice?'bg-t-light ':' Bg-main'" class=" br-round-right d-flex align-items-center p-75   justify-content-center col-6 " @click="notice = !notice">
                  <div class=" Fs0-1 text-center color-main text-nowrap  "  :class = "notice?' color-main  ':'text-white'">
                    اعلان تصویری
                  </div>
                </div>

                <div  :class = "notice?'Bg-main ':'bg-t-light'" class="  br-round-left d-flex align-items-center p-75   justify-content-center col-6"    @click="notice = !notice">
                  <div class=" Fs0-1 text-center   text-nowrap"  :class = "notice?'text-white ':'color-main'">
                   اعلان متنی
                  </div>
                </div>
              </b-col>
            </b-row>


            <base-block content-full>
              <b-form v-show="notice">
                <b-row class="push">
                  <b-col cols="4" >
                    <b-form-group label="تاریخ اتمام" label-for="example-text-input" class="Fs0-1">
                      <b-form-input id="example-text-input"   class="br-round" size="sm" ></b-form-input>
                    </b-form-group>
                  </b-col>
                  <b-col cols="8" >
                    <b-form-group label="عنوان" label-for="example-email-input" class="Fs0-1">
                      <b-form-input id="example-email-input " type="email"   class="br-round"  size="sm"></b-form-input>
                    </b-form-group>
                  </b-col>
                  <b-col cols="12" >
                  <b-form-group label="متن اعلان" label-for="example-textarea-input" class="Fs0-1">
                    <b-form-textarea id="example-textarea-input" rows="6"  class="form-control br-round"></b-form-textarea>
                  </b-form-group>
                  </b-col>
                  <b-col sm="8" class="  d-flex  pr-0 align-items-center mr-auto justify-content-end" >
                    <div class="  br-round d-flex align-items-center p-05 mt-3 justify-content-center ">
                      <a class="Fs0-2 color-main ml-2  " href="" style="text-decoration: underline">مشاهده صفحه اعلان</a>
                    </div>

                    <div class="Bg-submit br-round d-flex align-items-center  mt-3 justify-content-center ">
                      <p class="Fs0-2 text-white mb-0 text-nowrap">مشاهده جزییات</p>
                    </div>
                  </b-col>

                </b-row>

              </b-form>

              <b-form v-show="!notice">
                <b-row class="push">
                  <b-col cols="4" >
                    <b-form-group label="تاریخ اتمام" label-for="example-text-input" class="Fs0-1">
                      <b-form-input id="example-text-input"   class="br-round" size="sm" ></b-form-input>
                    </b-form-group>
                  </b-col>
                  <b-col cols="8" >
                    <b-form-group label="عنوان" label-for="example-email-input" class="Fs0-1">
                      <b-form-input id="example-email-input " type="email"   class="br-round"  size="sm"></b-form-input>
                    </b-form-group>
                  </b-col>
                  <b-col cols="12" >


                    <b-form-group label="عنوان" label-for="choseFile" class="Fs0-1">
                      <div class="w-100" id="choseFile">
                        <label for="files" class="w-100 d-flex">
                            <span class="col-9 form-control form-control-sm   br-round">{{file.name}}</span>
                            <span class="col-2 form-control form-control-sm br-box-t Bg-main text-white mr-auto d-flex justify-content-center">انتخاب فایل</span>
                        </label>

                        <input id="files" style="visibility:hidden;" type="file" @change="getFile">
                      </div>
                    </b-form-group>



<!--                    <b-form-group label="Bootstrap’s Custom File Input" class="Fs0-1" label-for="example-file-input-custom">-->
<!--                      <b-form-file id="example-file-input-custom " class="Fs0-1"></b-form-file>-->
<!--                    </b-form-group>-->
<!--                    <FormGroup className="form-group  position-relative   w-100">-->
<!--                      <div className='d-flex justify-content-end'>-->
<!--                        <Label>-->
<!--                          <span> {label} </span>-->

<!--                          {/*<IntlMessages id={label} />*/}-->
<!--                        </Label>-->
<!--                      </div>-->
<!--                      <InputGroup className="mb-3">-->
<!--                        <CustomInput-->
<!--                          type="file"-->
<!--                          id="uploadImage"-->
<!--                          name="uploadImage"-->
<!--                          onChange={this.onChangeImage}-->
<!--                          label={this.state.name ||'انتخاب عکس'}-->
<!--                        />-->
<!--                        {/*<InputGroupAddon addonType="append">Upload</InputGroupAddon>*/}-->
<!--                      </InputGroup>-->

<!--                    </FormGroup>-->
                    <div>

                    </div>


<!--                    <b-form-group label="متن اعلان" label-for="example-textarea-input" class="Fs0-1 opacity-0">-->
<!--                      <b-form-textarea id="example-textarea-input" rows="6"  class="form-control br-round"></b-form-textarea>-->
<!--                    </b-form-group>-->
                  </b-col>
                  <b-col sm="8" class="  d-flex  pr-0 align-items-center mr-auto justify-content-end" >
                    <div class="  br-round d-flex align-items-center p-05 mt-3 justify-content-center ">
                      <a class="Fs0-2 color-main ml-2 pr-3 pl-3   " href="" style="text-decoration: underline">مشاهده صفحه اعلان</a>
                    </div>

                    <div class="Bg-submit br-round d-flex align-items-center  mt-3 justify-content-center ">
                      <p class="Fs0-2 text-white mb-0 text-nowrap  p-2">مشاهده جزییات</p>
                    </div>
                  </b-col>

                </b-row>

              </b-form>


            </base-block>

          </base-block>
        </b-col>
        <!-- END Latest Customers -->
        <!-- Latest Orders -->
        <b-col lg="7">
          <base-block title="آمار رزرو ها   " dir="rtl"  class="Fs4 text-right br-box-t p-0   position-relative " content-full>
            <b-row class="m-0" >

              <b-col sm="4" class="  mt-6 d-flex flex-column justify-content-beween h-100    pr-0 ">

                <h3 class="Fs0-2">تعداد سانس های رزرو شده ی روز </h3>
                <b-col sm="10" class="ml-auto  mt-2 pr-0" >
                  <div class="bg-t-light br-round d-flex align-items-center p-75 ">
                    <div class="col-8 Fs0-1 text-center color-main ">
                      56
                    </div>
                    <div class="col-4 Fs0-1 text-left color-main">
                      ساعت

                    </div>


                  </div>


                </b-col>
                <h3 class="Fs0-2 mt-2">درآمد حاصله در روز </h3>
                <b-col sm="10" class="ml-auto  mt-2 pr-0" >
                  <div class="bg-t-light br-round d-flex align-items-center p-75 ">
                    <div class="col-8 Fs0-1 text-center color-main ">
                      1,400,000
                    </div>
                    <div class="col-4 Fs0-1 text-left color-main">
                      تومن

                    </div>
                  </div>
                </b-col>
                <b-col sm="8" class="ml-auto mt-2  pr-0" >
                <div class="Bg-submit br-round d-flex align-items-center p-05 mt-3 justify-content-center pr-4 pl-4 ">
                  <p class="Fs0-2 text-white mb-0 text-nowrap">مشاهده جزییات</p>
                </div>
                </b-col>

              </b-col>

              <b-col sm="8">
                <div class="py-3">
                  <chartjs-bar :chart-data="chartjsEarningsData" :options="chartjsOptions"></chartjs-bar>
                </div>
              </b-col>
            </b-row>

          </base-block>
        </b-col>
        <!-- END Latest Orders -->

      </b-row>
      <!-- END Customers and Latest Orders -->
    </div>
    <!-- END Page Content -->
  </div>
</template>


<script>

  // Chart.js, https://www.chartjs.org
  import Chart from 'chart.js'

  // Line Chart component using Vue Chart.js, for more info and examples you can check out https://github.com/apertureless/vue-chartjs
  // import ChartjsLine from '@/components/Chartjs/Line'
  import ChartjsBar from '@/components/Chartjs/Bar'
  import HeaderBoxField from "./Sub-content/Header-box-field/Header-box-field";

  import BoxNameCountDown from "./Sub-content/Box-name-countDown/Box-name-countDown";
  // import ChartjsRadar from '@/components/Chartjs/Radar'


  export default {
    name: "Dashboard",
    components: {
      BoxNameCountDown,
      HeaderBoxField,
       ChartjsBar
    },
    data () {
      return {
        notice:true,
        file:"",
        number:1,form:true,
        chartjsOptions: {
          maintainAspectRatio: false
        },
        chartjsStyles: {
          position: 'relative',
          height: '344px'
        },

        chartjsEarningsData: {
          labels: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12', '13', '14', '15', '16', '17', '18', '19', '20','21', '22', '23', '24'],
          datasets: [
            {
              label: 'تعداد رزرو',
              fill: true,
              // backgroundColor: 'rgba(132, 94, 247, .3)',
              backgroundColor: [
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',
                'rgba(160, 157, 166 )',
                'rgba(52, 50, 64 )',

              ],
              borderColor: 'transparent',
              borderWidth: 0,
              pointBackgroundColor: 'rgba(132, 94, 247, 1)',
              pointBorderColor: '#fff',
              pointHoverBackgroundColor: '#fff',
              pointHoverBorderColor: 'rgba(132, 94, 247, 1)',
              data: [0,2,3,4,3,4,2,5,3,4,2,3,4,5,3,2,2,4,2,3,2,1,2,3]
            },

          ]
        },

        latestCustomers: [
          {
            id: 1521,
            avatar: 'avatar11',
            name: 'هوشنگ مرادی',
            orders: "18:20"
          },
          {
            id: 1520,
            avatar: 'avatar1',
            name: 'ارتا زین الدین',
            orders: "18:20"
          },
          {
            id: 1519,
            avatar: 'avatar5',
            name: 'هوشنگ مرادی',
            orders: "18:20"
          },
          {
            id: 1518,
            avatar: 'avatar12',
            name: 'ارتا زین الدین',
            orders: "18:20"
          },   {
            id: 1518,
            avatar: 'avatar12',
            name: 'Ryan Flores',
            orders: "18:20"
          }
        ],
        latestOrders: [
          {
            id: 7835,
            date: 'today',
            state: 'Pending..',
            stateVariant: 'warning',
            total: '$999,99'
          },
          {
            id: 7834,
            date: 'today',
            state: 'Pending..',
            stateVariant: 'warning',
            total: '$2.299,00'
          },
          {
            id: 7833,
            date: 'today',
            state: 'Success',
            stateVariant: 'success',
            total: '$1200,00'
          },
          {
            id: 7832,
            date: 'today',
            state: 'Cancelled',
            stateVariant: 'danger',
            total: '$399,00'
          },
          {
            id: 7831,
            date: 'today',
            state: 'Success',
            stateVariant: 'success',
            total: '$349,00'
          },
          {
            id: 7830,
            date: 'today',
            state: 'Success',
            stateVariant: 'success',
            total: '$999,00'
          },
          {
            id: 7829,
            date: 'today',
            state: 'Success',
            stateVariant: 'success',
            total: '$39,99'
          },
          {
            id: 7828,
            date: 'today',
            state: 'Success',
            stateVariant: 'success',
            total: '$499,00'
          },
          {
            id: 7827,
            date: 'today',
            state: 'Success',
            stateVariant: 'success',
            total: '$325,00'
          }
        ]
      }
    },
    created () {
      // Set Chart.js configuration
      Chart.defaults.global.defaultFontColor              = 'rgba(52, 50, 64 )'
      Chart.defaults.global.defaultFontStyle              = '600'
      Chart.defaults.scale.gridLines.color                = "rgba(0,0,0,.05)"
      Chart.defaults.scale.gridLines.zeroLineColor        = "rgba(0,0,0,.1)"
      Chart.defaults.scale.display                        = true
      Chart.defaults.scale.ticks.beginAtZero              = true
      Chart.defaults.scale.ticks.stepSize                 = 1
      Chart.defaults.global.elements.line.borderWidth     = 2
      Chart.defaults.global.elements.point.radius         = 4
      Chart.defaults.global.elements.point.hoverRadius    = 6
      Chart.defaults.global.tooltips.cornerRadius         = 3
      Chart.defaults.global.legend.labels.boxWidth        = 15
    },
    methods: {
      getFile(event) {
        console.log(event.target.files);
       this.file=event.target.files[0]
      }
    }
  }
</script>
