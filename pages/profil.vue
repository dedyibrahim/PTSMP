<template>
  <v-sheet class="bg-white">
    <v-container>
      <v-row class="my-16">
        <v-col cols="12" md="6" sm="6" xs="6"    @transition-enter="onEnter"
          @transition-leave="onLeave">
          <p class="text-h6 font-weight-bold text-ungu">About Us</p>
          <p class="text-h4 font-weight-bold text-primary">
            PT Solusi Mitra Pertama
          </p>
          <br />
          <p class="text-h6 text-grey-darken-4 text-justify">
            Perusahaan kami bergerak dibidang pengadaan Barang dan Jasa,
            Khususnya Jasa Outsorcing. <br />
            Bagi Kami Kepuasan Klien Adalah prioritas yang sangat penting dan
            kami selalu merespon semua masukan dari klien kami secara serius dan
            tidak akan ragu mengambil tindakan yang diperlukan untuk menjaga
            reputasi kami sebagai salah satu perusahaan penyedia jasa outsorcing
            di Indonesia
          </p>
        </v-col>
        <v-col cols="12" md="6" sm="6" xs="6">
          <v-img height="auto" class="rounded-lg" src="../public/images/profile.jpg" />
        </v-col>
      </v-row>
    </v-container>
  </v-sheet>

  <v-sheet class="bg-grey-lighten-2">
    <v-container>
      <v-row class="my-16">
        <v-col cols="12" md="6" sm="12" xs="12">
             <p class="text-center text-h3 text-primary font-weight-bold ">Visi</p>
              <p class="text-h6 text-justify mt-4">Menjadi Perusahaan Penyedia TAD dan SDM Yang professional Terpercaya, Terpilih dan Berkualitas</p>
        </v-col>
        <v-col cols="12" md="6" sm="12" xs="12">
             <p class="text-center text-h3 text-primary font-weight-bold">Misi</p>
             <p class="text-h6 text-justify mt-4">Peningkatan Kualitas, Kuantitas, dan Variasi Produk dengan tetap mempertahankan Input sumber daya yang ada dengan menjalankan proyek yang efisien dari segi waktu dan biaya dengan dukungan tim yang solid.</p>
        </v-col>
      </v-row>
 
    </v-container>
  </v-sheet>

  <v-parallax height="300px" src="/images/indobuild.png">
    <v-sheet class="bg-transparent">
      <v-container>
        <v-row class="my-16">
          <v-col cols="12" md="12" sm="12" xs="12">
            <p class="text-h5 text-center font-weight-bold text-white">
              Solusi outsourcing terdepan untuk mempercepat pertumbuhan bisnis Anda. Tim kami ahli dalam mengelola tugas-tugas terkait sumber daya manusia, keuangan, dan teknologi, membebaskan Anda untuk fokus pada inti bisnis Anda.
            </p>
           
          </v-col></v-row></v-container></v-sheet>
  </v-parallax>

  <v-sheet class="bg-grey-lighten-3">
    <v-container>
      <v-row class="my-16">
        <v-col cols="12" md="12" sm="12" xs="12">
          <p class="text-h4 text-center font-weight-bold text-primary">
            Klien Kami
          </p>
          <p class="text-h6 text-center text-grey-darken-3">
            PT Solusi Mitra Pertama telah dipercaya berbagai bisnis lintas
            industri
          </p>

          <v-row>
            <v-col   cols="12" sm="1" xs="1" md="2" v-for="n in 14">
              <v-hover v-slot="{ isHovering, props }">
              <v-card class="mx-auto mt-5 elevation-0 bg-transparent my-auto"   v-bind="props"
                    :elevation="isHovering ? 12 : 2" 
                    :class="{
                      'text-primary on-hover  animate__animated animate__pulse':
                        isHovering,
                    }">
                  <v-img  width="120px" cover class="rounded-lg my-auto" :src="'/images/client/' + n + '.png'" />
              </v-card>
            </v-hover>
            </v-col>
          </v-row>
        </v-col></v-row></v-container></v-sheet>
</template>

<script>
export default {
  methods: {
    onEnter(el, done) {
      alert("Asdsad")
      this.animateClass = true;
      setTimeout(done, 1000); // Mengatur durasi animasi (1 detik)
    },
    onLeave(el, done) {
      this.animateClass = false;
      setTimeout(done, 1000); // Mengatur durasi animasi (1 detik)
    },
  },
  data() {
    return {
      dataPekerjaan: [
        {
          title: "WareHouse",
          icon: "/images/warehouse.png",
          listWork: [
            { name: "Staf Gudang" },
            { name: "Operator Warehouse" },
            { name: "Admin Gudang" },
            { name: "Kepala Gudang" },
            { name: "Packer" },
          ],
        },
        {
          title: "Logistik",
          icon: "/images/logistik.png",
          listWork: [
            { name: "Kurir" },
            { name: "Delivery" },
            { name: "Driver" },
            { name: "Kurir Event" },
            { name: "Kurir Harian" },
          ],
        },
        {
          title: "Penjualan & Pelayanan",
          icon: "/images/penjualan.png",
          listWork: [
            { name: "Field Sales" },
            { name: "Telemarketer" },
            { name: "Business Development" },
            { name: "Customer Service" },
            { name: "SPG/SPB" },
          ],
        },
        {
          title: "Manufaktur",
          icon: "/images/manufaktur.png",
          listWork: [
            { name: "Security" },
            { name: "Pekerja Lepas" },
            { name: "Operator Produksi" },
            { name: "Teknisi" },
            { name: "Helper Produksi" },
          ],
        },
        {
          title: "Konstruksi & Bangunan",
          icon: "/images/kontruksi.png",
          listWork: [
            { name: "Surveyor" },
            { name: "Pekerja Konstruksi" },
            { name: "Tenaga ahli" },
            { name: "Estimator" },
            { name: "Dll" },
          ],
        },
        {
          title: "Dapur & Pantri",
          icon: "/images/chef.png",
          listWork: [
            { name: "Chef" },
            { name: "Cook Helper" },
            { name: "Kitchen Crew" },
            { name: "Head Chef" },
            { name: "Dll" },
          ],
        },
        {
          title: "Hotel & Restaurant",
          icon: "/images/hotel.png",
          listWork: [
            { name: "Waiter & Waiters" },
            { name: "Operator Warehouse" },
            { name: "Front Office" },
            { name: "Resepsionis" },
            { name: "Room Service" },
          ],
        },
        {
          title: "Kebersihan",
          icon: "/images/kebersihan.png",
          listWork: [
            { name: "Cleaning Service" },
            { name: "Office Boy" },
            { name: "Graderner" },
            { name: "Sky Service" },
            { name: "House Keeping" },
          ],
        },
      ],
    };
  },
};
</script>
