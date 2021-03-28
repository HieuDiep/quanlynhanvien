<template>
    
    <div id="content">
        
        <div class="page-title">
            <div class="page-left">Danh sách khách hàng</div>
            <div class="page-right">
                <button id="btnAdd" @click="showForm" class="btn-default">Thêm khách hàng</button>
            </div>
        </div>
        <div class="toolbar">
            <input type="text" class="input-search" style="width: 220px;" placeholder="Tìm kiếm theo mã, tên khách hàng" />
            <button class="btn-refresh"></button>
            <button class="btn-delete"></button>
        </div>
        <div class="grid">
            <table id="tblListCustomer" class="table" width="100%" border="0">
                <thead>
                    <tr>
                        <th>Mã khách hàng</th>
                        <th>Họ và tên</th>
                        <th>Giới tính</th>
                        <th>Ngày sinh</th>
                        <th>Nhóm khách hàng</th>
                        <th>Điện thoại</th>
                        <th>Email</th>
                        <th class="text-align-right">Số tiền nợ</th>
                        <th class="text-align-center">Đang hoạt động</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>KH0001</td>
                        <td>Nguyễn Văn Mạnh</td>
                        <td>Nam</td>
                        <td>22/09/1999</td>
                        <td>VIP</td>
                        <td>0961179969</td>
                        <td>manhnv229@gmail.com</td>
                        <td  class="text-align-right">1.025.000</td>
                        <td class="text-align-center"><input type="checkbox" checked></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="paging" v-if="!show">
            <div data-v-a72348a4="" class="paging-bar"><div data-v-a72348a4="" class="paging-record-info">Hiển thị <b data-v-a72348a4="">1-10/1000</b> nhân viên</div><div data-v-a72348a4="" class="paging-option"><div data-v-a72348a4="" class="btn-select-page m-btn-firstpage"></div><div data-v-a72348a4="" class="btn-select-page m-btn-prev-page"></div><div data-v-a72348a4="" class="m-btn-list-page"><button data-v-a72348a4="" class="btn-pagenumber btn-pagenumber-selected">1</button><button data-v-a72348a4="" class="btn-pagenumber">2</button><button data-v-a72348a4="" class="btn-pagenumber">3</button><button data-v-a72348a4="" class="btn-pagenumber">4</button></div><div data-v-a72348a4="" class="btn-select-page m-btn-next-page"></div><div data-v-a72348a4="" class="btn-select-page m-btn-lastpage"></div></div><div data-v-a72348a4="" class="paging-record-option"><b data-v-a72348a4="">10</b> nhân viên/trang</div></div>
        </div>
        <div class="" v-if="show">
            <add-customers @close="showForm">  
            </add-customers>
        </div>
    </div>
</template>
<script>
import addCustomers from '../form/addCustomers.vue';
export default {
  components: { addCustomers },
    name:'theContent',
    comments:{addCustomers},
    data() {
        return {
            show:false,
        }
    },

    methods:{
        showForm(){
            console.log("hello")
            return this.show =!this.show ;
        },
    }
}
</script>
<style scoped>
@import url('../../style/base/input.css');
#content{
    position: absolute;
    top: 60px;
    left: 200px;
    right: 0px;
    bottom: 0px;
    /* background-color: yellow; */
    /* padding-left:  24px; */
    padding: 24px;
}

#content .paging-bar {
    height: 56px;
}

.paging-bar {
    border-top: 1px solid #bbbbbb;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0 16px;
    z-index: 1 !important;
}

.btn-pagenumber.btn-pagenumber-selected, .btn-pagenumber-selected:hover {
    background-color: #019160;
    color: #ffffff;
}

.btn-pagenumber {
    width: 30px;
    height: 30px;
    margin: 0 4px;
    border: 1px solid #ccc;
    border-radius: 50%;
    background-color: #e9ebee;
    cursor: pointer !important;
}

.paging-bar .paging-record-info {
    position: absolute;
    left: 16px;
}

.paging-bar .paging-record-option {
    position: absolute;
    right: 16px;
}

.page-title{height: 40px;display: flex;align-items: center;}

.page-title .page-right{
    position:  absolute;
    right: 24px;
}

.page-title .page-left{
    font-size: 24px;
    font-weight:bold;
}


.toolbar{
    margin-top: 16px;
    display: flex;
    width: 100%;
    align-items: center;
    height: 42px;
    /* background-color: #ff0000; */
}

.grid{
    position: absolute;
    right:  24px;
    left: 24px;
    bottom: 60px;
    top: 128px;
    overflow-y: auto;
}

.paging{
    position: absolute;
    bottom:0;
    height: 60px;
    left: 24px;
    right: 24px;
}

.m-col{
width: 50%;
float: left;
padding: 0 4px;
box-sizing: border-box;
}

</style>