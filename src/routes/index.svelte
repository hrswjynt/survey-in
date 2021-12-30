<script>
	let surveys = [
		{
			nama: 'Komp. Agung Mulya',
			lokasi: 'Jln. Ahmad Yani',
			jumlah_rumah: [{ developer: 1 }, { swadaya: 4 }]
		},
		{
			nama: 'Komp. Puranam 1',
			lokasi: 'Jln. Ahmad Yani',
			jumlah_rumah: [{ developer: null }, { swadaya: 5 }]
		},
		{
			nama: 'Komp. Bhayangkara',
			lokasi: 'Jln. Ahmad Yani',
			jumlah_rumah: [{ developer: 1 }, { swadaya: null }]
		}
	];
</script>

<table>
	<tr>
		<td>
			<label for="nama">
				<span class="block">Nama Gang/Perumahan</span>
			</label>
		</td>
		<td>
			<input id="nama" class="m-1 border-2" type="text" />
		</td>
	</tr>
	<tr>
		<td>
			<label for="lokasi">
				<span class="block">Lokasi</span>
			</label>
		</td>
		<td>
			<input id="lokasi" class="m-1 border-2" type="text" />
		</td>
	</tr>
	<tr>
		<td>
			<label for="developer">
				<span class="block">Developer</span>
			</label>
		</td>
		<td>
			<input id="developer" class="m-1 border-2" type="number" />
		</td>
	</tr>
	<tr>
		<td>
			<label for="swadaya">
				<span class="block">Swadaya</span>
			</label>
		</td>
		<td>
			<input id="swadaya" class="m-1 border-2" type="number" />
		</td>
	</tr>
	<tr>
		<td colspan="2">
			<button class="btn btn-full btn-blue">Submit</button>
		</td>
	</tr>
</table>

<table class="table">
	<tr>
		<th rowspan="2" class="border-2 px-2">Nama Gang/Perumahan</th>
		<th rowspan="2" class="border-2 px-2">Lokasi</th>
		<th colspan="2" class="border-2 px-2">Jumlah Rumah</th>
	</tr>
	<tr>
		<th class="border-2 px-2">Developer</th>
		<th class="border-2 px-2">Swadaya</th>
	</tr>
	{#each surveys as survey}
		<tr>
			<td class="border-2 px-2">{survey.nama}</td>
			<td class="border-2 px-2">{survey.lokasi}</td>
			<td class="border-2 px-2">{survey.jumlah_rumah[0].developer}</td>
			<td class="border-2 px-2">{survey.jumlah_rumah[1].swadaya}</td>
		</tr>
	{/each}
</table>
