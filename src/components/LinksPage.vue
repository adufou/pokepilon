<script setup lang="ts">
import {
  Table, TableHeader, TableBody, TableRow, TableHead, TableCell,
} from '@/components/ui/table'

const links = [
  {
    name: 'Type Chart',
    desc: 'Tableau croisé des types de pokémons',
    url: 'https://upload.wikimedia.org/wikipedia/commons/9/97/Pokemon_Type_Chart.svg',
  },
  {
    name: 'Niveaux des minerais',
    desc: 'Tableau des meilleurs niveaux Y pour miner chaque minerai dans Minecraft',
    url: 'https://www.reddit.com/r/Minecraft/comments/zc0w46/i_made_a_simple_chart_to_know_which_are_the_best/',
  },
  {
    name: 'Biome Finder',
    desc: 'Localiser les biomes de notre monde Minecraft (seed incluse)',
    url: 'https://www.chunkbase.com/apps/biome-finder#seed=-6762404268818883586&platform=java_1_21_5&dimension=overworld',
  },
  {
    name: 'Wiki Cobblemon',
    desc: 'Wiki officiel du mod Cobblemon : Pokémon, mécaniques, objets et plus',
    url: 'https://wiki.cobblemon.com/index.php/Main_Page',
  },
  {
    name: 'Pokédex Cobblemon',
    desc: 'Pokédex complet avec stats, capacités et infos pour Cobblemon',
    url: 'https://cobblemon.tools/pokedex/',
  },
  {
    name: 'Drive Cobblemon 1.7.3',
    desc: 'Dossier Google Drive pour Cobblemon 1.7.3',
    url: 'https://drive.google.com/drive/folders/1FaKtUQQ5gikqIfcy_k-xT8lejOtyJQfK',
  },
  {
    name: 'Équivalences spawn/biome Cobblemon',
    desc: 'Conditions de spawn des Pokémon par biome dans Cobblemon (wiki officiel)',
    url: 'https://wiki.cobblemon.com/index.php/Pok%C3%A9mon/Spawning/Spawn_Definitions',
  },
  {
    name: 'Spawns Cobblemon',
    desc: 'Spreadsheet des zones et conditions de spawn des Pokémon (1.7.3)',
    url: 'https://docs.google.com/spreadsheets/d/1DJT7Hd0ldgVUjJbN0kYQFAyNBP6JGG_Clkipax98x-g/edit?gid=0#gid=0',
  },
  {
    name: 'Drops Cobblemon',
    desc: 'Liste des objets droppés par chaque Pokémon dans Cobblemon (1.7.3)',
    url: 'https://docs.google.com/spreadsheets/d/1EG8-VxLukiGWonM7e9J_DH0ZAVdkWo3W64bP2jT6koo/edit?gid=0#gid=0',
  },
  {
    name: 'Guide des évolutions',
    desc: 'Conditions d\'évolution de tous les Pokémon Cobblemon',
    url: 'https://www.cobbledex.info/evolution-guide',
  },
  {
    name: 'Arènes Kanto',
    desc: 'Guide des champions d\'arène de Kanto sur Cobbleverse',
    url: 'https://www.lumyverse.com/cobbleverse/kanto-gym-leaders/',
  },
  {
    name: 'Légendaires & Mythiques',
    desc: 'Guide pour capturer tous les Pokémon légendaires et mythiques sur Cobbleverse',
    url: 'https://www.lumyverse.com/cobbleverse/how-to-catch-all-legendary-mythical-pokemon/',
  },
]
</script>

<template>
  <div class="p-16">
    <Table>
      <TableHeader>
        <TableRow>
          <TableHead>Nom</TableHead>
          <TableHead>Description</TableHead>
          <TableHead>Lien</TableHead>
        </TableRow>
      </TableHeader>
      <TableBody>
        <TableRow v-for="link in links" :key="link.url">
          <TableCell>{{ link.name }}</TableCell>
          <TableCell>{{ link.desc }}</TableCell>
          <TableCell>
            <a
              :href="link.url"
              target="_blank"
              rel="noopener noreferrer"
              class="text-primary underline underline-offset-4 hover:opacity-80"
            >
              {{ link.url }}
            </a>
          </TableCell>
        </TableRow>
      </TableBody>
    </Table>
  </div>
</template>
