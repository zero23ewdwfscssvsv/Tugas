package main

import  (
	 "fmt"
)

type nama barang struct {
	      nama string
	      harga int
}

func main()
	 barang := []barang{
	 barang{nama: "Fun Cooler Smartphone", harga: 150000},
	 barang{nama: "Game Pad Rexus", harga: 400000},
	 barang{nama:"Headshet Qxz", harga : 200000},
}
	//list harga
	fmt.Println("\n Harga")
	for i, barang := range barangs {
	 fmt.printf("%v. %v : Rp %v\n", i+1, barang,nama,barang,harga)
		}

		 var transaksi string
		  total := 0

		  for {
			var pilihBarang, qty, subtotal int

			// pilihan 0 exit
			if pilihBarang == 0 {
				break
		         }
			//input barang
			fmt.Print("pilih barang 1 -3 atau '0' untuk exit :")
			-, err := fmt. Scanln(&pilihBarang)
			if err != nil {
                        	fmt.Println("interger only")
					return
		 	}
			// meriksa jika inputan tidak sesuai
			if pilihBarang < 1 || pilihBarang > len(barangs) { //len -> panjang barangs(3)
				 fmt.Print("Tolong pilih 1 - 3")
							continue
			}
			// qty
			fmt.Print("jumlah barang : ")
			_, error := fmt.Scanln(&qty)
			if error != nil {
						    			fmt.Println("Integer Only")
			return
			}
			// sesuaikan angka pilihan 012 -> 123
			p := barangs[pilihBarang-1]
			subtotal = p.harga * qty

			// penggabungan transaksi
			transaksi += fmt. Sprintf("%v sebanyak %v harga nya Rp. %v\n, p.nama, qty, subtotal")

			// menampilkan transaksi
			fmt.Println(transaksi)

			//Total Harga akhir
			total += subtotal
			}
			//menampilkan total
			transaksi += fmt.Sprintf("Total : Rp %v\n", total)
			println(transaksi)
	}

	
