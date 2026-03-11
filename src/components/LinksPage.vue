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
