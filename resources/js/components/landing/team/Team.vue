<script setup lang="ts">
import { ref } from 'vue';
import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogHeader,
  DialogTitle,
  DialogTrigger,
} from '@/components/ui/dialog';

interface TeamMember {
  id: number;
  name: string;
  role: string;
  image: string;
  shortBio: string;
  modalContent?: string[];
  linkedIn?: string;
}

import ronaldoImg from '@/assets/Salunga.png';
import henryImg from '@/assets/henry.jpg';
// import joelImg from '@/assets/joel.jpg';
// import ReynaldoImg from '@/assets/reynaldo.jpg';
// import bobbyImg from '@/assets/bobbyrekhi.jpeg';
// import aliImg from '@/assets/Ali-2.jpeg';
// import jayImg from '@/assets/jay.jpeg';

const team = ref<TeamMember[]>([
  {
    id: 1,
    name: 'Ronaldo M. Salunga, CESE',
    role: 'President CEO',
    image: ronaldoImg,
    shortBio:
      'Ronaldo M. Salunga, CESE, is a seasoned executive, technopreneur, and former senior government official with over three decades of leadership experience spanning public administration, transportation modernization, information technology, agriculture systems, and green mobility innovation...',
    modalContent: [
      'Ronaldo M. Salunga, CESE, is a seasoned executive, technopreneur, and former senior government official with over three decades of leadership experience spanning public administration, transportation modernization, information technology, agriculture systems, and green mobility innovation.',
      'He is the Co-Founder and incumbent General Manager of <strong>Device Design Green and Smart Corporation</strong>, where he leads the development of intelligent, sustainable, and technology-driven solutions for infrastructure, mobility, and digital systems.',
      'Mr. Salunga also co-founded <strong>CMW Philippines</strong> in partnership with a Silicon Valley-based technopreneur. The company successfully secured government accreditation to distribute and sell Class 3 Modern Jeepneys in support of the national Public Utility Vehicle Modernization Program under the <strong>Department of Transportation Philippines</strong>.',
      '<strong>Public Service Leadership</strong> <br> Before entering private enterprise, Mr. Salunga dedicated nearly 20 years to public service, holding key executive positions in the Philippine government:',
      '<ul class="list-disc list-inside"><li>Presidential Staff Officer, Presidential Management Staff – Office of the President (1990–2003)</li><li>Assistant Director, <strong>Agricultural Training Institute</strong></li><li>Executive Director, <strong>Land Transportation Franchising and Regulatory Board</strong></li><li>Executive Director, <strong>Information Technology Center for Agriculture and Fisheries</strong></li></ul>',
      'His appointments during the administration of <strong>Gloria Macapagal-Arroyo</strong> reflect his trusted role in advancing national reforms in transport regulation, digital agriculture, and government systems modernization.',
      '<strong>Global Technology & Mobility Engagement</strong> <br> Mr. Salunga’s international and private-sector leadership includes:',
      '<ul class="list-disc list-inside"><li><strong>President, NWire Technology Consortium</strong>, representing U.S.-based wireless technology innovators</li> <li>Board Director, <strong>California Mobility Works</strong> (Santa Clara, California)</li> <li>President & CEO (2018–2024), <strong>Eltrans Innovators Inc.</strong>, an electric vehicle solutions provider</li> <li>Chairman (2018–Present), <strong>Centerstar Insurance Agency and Management Corporation</strong></li></ul>',
      '<strong>Leadership Vision</strong> <br> Mr. Salunga brings together deep government insight and private-sector innovation to advance:',
      '<ul class="list-disc list-inside"><li>Smart and sustainable mobility ecosystems</li> <li>Public transport modernization</li> <li>Digital agriculture transformation</li></ul>',
    ],
  },
  {
    id: 2,
    name: 'Henry V. Bayubay',
    role: 'Chief Technology Officer/ EVP',
    image: henryImg,
    linkedIn: 'https://www.linkedin.com/in/henry-b-a3867559/',
    shortBio:
      'Henry V. Bayubay is a distinguished Filipino entrepreneur, technology advocate, and business executive with over 35 years of experience in the information technology environment, currently serving as President and Chief Executive Officer of BB 88 Advertising and Digital Solutions Inc...',
    modalContent: [
      'Henry V. Bayubay is a distinguished Filipino entrepreneur, technology advocate, and business executive with over 35 years of experience in the information technology environment, currently serving as President and Chief Executive Officer of <strong>BB 88 Advertising and Digital Solutions Inc.</strong>, held several positions in media and digital solutions. He is also currently member of the <strong>Filipino Inventors Society Multi-Purposed Cooperative (FISMPC)</strong>. His extensive background spans advertising, digital transformation, enterprise IT systems, and integrated technology ecosystems, enabling him to lead innovative solutions that empower businesses, institutions, and communities across the Philippines.',
      'Under his leadership, BB 88 Advertising and Digital Solutions Inc. has evolved beyond traditional advertising into a multi-sector innovation company driving digital ecosystems, e-mobility solutions, trust and security systems, and smart precision farming technologies. These initiatives support agribusiness modernization, sustainable transportation, secure digital infrastructure, youth technology development, and smart community transformation.',
    ],
  },
  // {
  //   id: 3,
  //   name: 'Joel Sotomayor',
  //   role: 'Technology Partner',
  //   image: joelImg,
  //   linkedIn: 'https://www.linkedin.com/in/joel-sotomayor/',
  //   shortBio:
  //     'mPowered Technology Solutions Inc., - A Filipino-Canadian serial entrepreneur and inventor, Joel Sotomayor holds six patents across ten jurisdictions, 2 Canadian Trademarks, and has earned multiple international innovation awards in agriculture from Canada and Australia....',
  //   modalContent: [
  //     '<strong>mPowered Technology Solutions Inc.</strong>, - A Filipino-Canadian serial entrepreneur and inventor, Joel Sotomayor holds six patents across ten jurisdictions, 2 Canadian Trademarks, and has earned multiple international innovation awards in agriculture from Canada and Australia.',
  //     'He pioneered: <br/> <ul class="list-disc list-inside"><li>Created IoT sensors to improve livestock welfare during land and sea transport,</li><li>Is part of a Canadian consortium that has developed a flexible microgrid systems that grant energy sovereignty to rural communities,</li><li>Developed low-cost smart sensors that enable banana producers to digitize farm operations, increase yields, and reduce biosecurity risks, and</li><li>Has developed a novel lightweight encryption protocol to provide data provenance and has been recently completed a research project via a Canadian University to protect drone signals from hacking Joel’s work reflects a mission beyond invention empowering communities through accessible, sustainable technologies.</li></ul>',
  //   ],
  // },
  // {
  //   id: 4,
  //   name: 'Reynaldo Sanchez',
  //   role: 'Director',
  //   image: ReynaldoImg,
  //   shortBio:
  //     'Reynaldo C. Sanchez is a Filipino business leader, media executive, and corporate officer known for leadership across multiple companies in media, mobility, development, and digital entertainment sectors....',
  //   modalContent: [
  //     '<strong>Reynaldo C. Sanchez</strong> is a Filipino business leader, media executive, and corporate officer known for leadership across multiple companies in media, mobility, development, and digital entertainment sectors.',
  //     '<ul class="list-disc list-inside"><li><strong>Chairman, E-Pinoy Mobility System Inc.</strong> - EMSi is a Philippine-based mobility company focused on operating and managing electric transport systems supported by modern digital platforms.</li><li><strong>President and CEO of Asian Television Content Corporation</strong> - A Philippine television content company responsible for programming and broadcast content, notably in partnerships with networks like IBC 13.</li><li><strong>Chairman of the Board, Esports World Federation (ESWF)</strong> - He is listed as Chairman of the Board of this international esports and digital sports governance organization.</li></ul>',
  //     'Reynaldo C. Sanchez is publicly identifiable as a professional engineer, corporate leader involved in broadcast media and digital entertainment governance, blending roles in traditional television distribution with emerging digital and esports platforms.',
  //     '<ul class="list-disc list-inside"><li>Wireless and emerging technologies integration</li><li>Green infrastructure and intelligent systems development</li></ul>',
  //     'His leadership reflects a lifelong commitment to nation-building through technology, governance reform, and sustainable enterprise development.',
  //   ],
  // },
  // {
  //   id: 5,
  //   name: 'Bobby Rekhi',
  //   role: 'Managing General Partner',
  //   image: bobbyImg,
  //   shortBio:
  //     'Silicon Valley veteran and early venture ecosystem pioneer. Key contributor to multiple success stories including AudioHighway (Nasdaq), TestDrive Systems, CyberPlus, and Mars Communications acquisitions.',
  //   linkedIn: 'https://www.linkedin.com/in/bobby-rekhi-91a5a22/',
  // },
  // {
  //   id: 6,
  //   name: 'Ali Bushehri',
  //   role: 'Managing General Partner',
  //   image: aliImg,
  //   shortBio:
  //     'Leads M&A and fundraising strategies with 35+ years of executive leadership in high-tech and fintech. Active investor connected to a global network of top-tier financiers.',
  //   linkedIn: 'https://www.linkedin.com/in/ali-bushehri-8291121/',
  // },
  // {
  //   id: 7,
  //   name: 'Jay Amaran',
  //   role: 'Managing General Partner · India',
  //   image: jayImg,
  //   shortBio:
  //     'IIT Madras, IIM Ahmedabad, and MIT Cambridge alumnus with 44+ years in coding and consulting, including 27 years with the World Bank. Pioneer in early spreadsheet algorithms, co-creator of the Y2K DA-TE-2000 fix, and innovator in predictive analytics and genetic computing. Active investor and mentor across software, healthcare, agriculture, realty, and education sectors.',
  //   linkedIn: 'https://www.linkedin.com/in/jay78iit80iim96mit/',
  // },
]);
</script>

<template>
  <section class="mx-auto max-w-7xl px-6 pt-3 pb-16">
    <!-- Section Header -->
    <div class="mb-8 flex w-full items-center gap-4">
      <div class="grow border-t-2 border-bright-green"></div>
      <span
        class="shrink-0 text-xl font-bold tracking-widest text-bright-green uppercase"
      >
        OUR TEAM
      </span>
      <div class="grow border-t-2 border-bright-green"></div>
    </div>

    <!-- Team Cards -->
    <div class="grid justify-center gap-8 pt-5 md:grid-cols-2">
      <div
        v-for="member in team"
        :key="member.id"
        class="flex flex-col rounded-4xl border border-emerald-50/50 bg-white p-5 shadow-md shadow-emerald-100 transition-shadow hover:shadow-lg sm:p-8"
      >
        <!-- Header -->
        <div
          class="mb-6 items-center text-center sm:flex sm:gap-4 sm:text-left"
        >
          <div
            class="mx-auto h-50 w-50 shrink-0 overflow-hidden rounded-xl border-2 border-emerald-100 sm:mx-0 sm:h-30 sm:w-30"
          >
            <img
              :src="member.image"
              :alt="member.name"
              class="h-full w-full object-cover"
            />
          </div>
          <div>
            <h4 class="pt-4 text-xl font-bold text-bright-green sm:pt-0">
              {{ member.name }}
            </h4>
            <p
              class="pt-1 text-sm font-medium tracking-wider text-gray-400 uppercase"
            >
              {{ member.role }}
            </p>
          </div>
        </div>

        <!-- Short Bio -->
        <p class="text-base leading-relaxed text-gray-700">
          {{ member.shortBio }}
        </p>

        <!-- Actions -->
        <div class="grid">
          <Dialog v-if="member.modalContent">
            <DialogTrigger as-child>
              <div class="text-end">
                <button
                  class="cursor-pointer text-sm font-semibold text-bright-green hover:underline"
                >
                  Read More
                </button>
              </div>
            </DialogTrigger>

            <DialogContent
              class="flex max-h-[90vh] flex-col overflow-hidden p-0 sm:max-w-3xl"
            >
              <DialogHeader class="shrink-0 border-b px-6 py-4">
                <DialogTitle class="text-xl font-bold text-bright-green">
                  {{ member.name }}
                </DialogTitle>
                <DialogDescription
                  class="pt-1 text-sm font-medium tracking-wider text-gray-400 uppercase"
                >
                  {{ member.role }}
                </DialogDescription>
              </DialogHeader>

              <div class="flex-1 overflow-y-auto px-6">
                <p
                  v-for="(paragraph, i) in member.modalContent"
                  :key="i"
                  v-html="paragraph"
                  class="mb-4 text-base leading-relaxed text-gray-700"
                ></p>
              </div>

              <div class="shrink-0 border-t px-6 py-4 text-end">
                <DialogTrigger as-child>
                  <button
                    class="w-fit cursor-pointer rounded bg-bright-green px-4 py-2 text-white hover:bg-emerald-700"
                  >
                    Close
                  </button>
                </DialogTrigger>
              </div>
            </DialogContent>
          </Dialog>

          <a
            v-if="member.linkedIn"
            :href="member.linkedIn"
            target="_blank"
            class="mt-6 text-sm font-semibold text-bright-green hover:underline"
          >
            LinkedIn →
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
