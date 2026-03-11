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
    name: 'Drops Cobblemon',
    desc: 'Liste des objets droppés par chaque Pokémon dans Cobblemon',
    url: 'https://wiki.cobblemon.com/index.php/Pok%C3%A9mon/Drops',
  },
  {
    name: 'Pokédex Cobblemon',
    desc: 'Pokédex complet avec stats, capacités et infos pour Cobblemon',
    url: 'https://cobblemon.tools/pokedex/',
  },
  {
    name: 'Spawns Cobblemon',
    desc: 'Spreadsheet des zones et conditions de spawn des Pokémon',
    url: 'https://docs.google.com/spreadsheets/d/1dldBZuUmQXUWbY2YOgNAIryjwXJqzHaNDly-a8Oml04/edit?pli=1&gid=0#gid=0',
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
