<template>
  <div>
    <div :class="state.open ? '-ml-2 flex justify-start mt-12' : 'flex justify-start ml-3 mt-12'">
      <cubes-icon class="mt-0.5" /> 
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14" title="Vacations" />
    </div>

    <Accordion v-if="state.open == false" class="-mt-4">
      <template #item>
        <chat-icon class="mt-0.5 -ml-2 mr-1" /> <span class="pl-3 text-sm">Request</span>
      </template>
      <template #panel>
        <sidenav-item class="text-xs" title="Create Request" />
        <sidenav-item class="text-xs" title="View All Request" />
        <sidenav-item class="text-xs" title="Bulk Request" />
        <sidenav-item class="text-xs" title="Download Range" />
        <sidenav-item class="text-xs" title="From Build" />
      </template>
    </Accordion>
    <div v-else>
      <chat-icon :class="state.open ? '-ml-2 mt-3' : ''" />
    </div>

    <Accordion v-if="state.open == false" class="-mt-4">
      <template #item>
        <pencil-icon class="-ml-2 mr-2" /> <span class="pl-3 text-sm">Signature Request</span>
      </template>
      <template #panel>
        <sidenav-item class="text-xs" title="Templates" />
        <sidenav-item class="text-xs" title="Custom Fields" />
      </template>
    </Accordion>
    <div v-else>
      <pencil-icon class="mt-3 -ml-2 mr-1" />
    </div>

    <div :class="state.open ? '-ml-2 mt-4' : 'flex ml-3 mt-2'">
      <contact-edit-icon class="mt-0.5 -mr-3" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-10" title="Document Request" />
    </div>

    <div :class="state.open ? '-ml-2 mt-4' : 'flex ml-3 mt-2'">
      <papers-icon class="mt-0.5 mr-1" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14" title="Data Request" />
    </div>
    
    <div :class="state.open ? '-ml-2 mt-4' : 'flex ml-3 mt-2'">
      <chat-message-icon class="mt-1 mr-1" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14" title="Message Template" />
    </div>

    <div :class="state.open ? '-ml-4 mt-3' : 'flex ml-2.5 mt-2'">
      <schedule-icon class="mt-0.5 ml-1 -ml-0.5" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14" title="Reminder Rule" />
    </div>

    <div :class="state.open ? '-ml-3.5 mt-3' : 'flex ml-2 mt-2'">
      <phone-icon class="mt-0.5" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14" title="Contacts" />
    </div>

    <div v-if="state.open == false" class="text-gray-300 ml-3 uppercase text-lg font-semibold mt-2">
      Client Management
    </div>

    <div :class="state.open ? '-ml-2 mt-3' : 'flex ml-3 mt-2'">
      <site-icon class="mt-0.5" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14" title="Sites" />
    </div>

    <div :class="state.open? '-ml-2 mt-2.5' : 'flex ml-3 mt-2'">
      <support-icon class="mt-0.5 -ml-2 mr-1" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-16" title="Support" />
    </div>
    
    <div :class="state.open ? '-ml-2 mt-2' : 'flex ml-3 mt-2'">
      <package-icon class="-ml-0.5" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14" title="Packages" />
    </div>

    <div v-if="state.open == false" class="text-gray-300 ml-3 mb-3 uppercase md:text-lg font-semibold">
      Misc
    </div>

    <div :class="state.open ? '-ml-0.5 mt-4' : 'flex ml-4 mt-2'">
      <users-icon class="-ml-1.5" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14 -mt-4" title="Users" />
    </div>

    <div :class="state.open ? '-ml-0.5 mt-4' : 'flex ml-4 mt-2'">
      <sms-icon class="-ml-1.5 -mr-1" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14 -mt-2" title="SMS" />
    </div>

    <div :class="state.open ? '-ml-2 mt-3' : 'flex ml-3 mt-2 pb-8'">
      <settings-icon class="-ml-0.5 -mr-1" />
      <sidenav-item v-if="state.open == false" class="text-sm -ml-14 -mt-2" title="Settings" />
    </div>

  </div>
</template>

<script>
import SidenavItem from './Item.vue'
import Accordion from './accordion/Accordion.vue'

/* ICONS */
import CubesIcon from './icons/Cubes.vue'
import ChatIcon from './icons/Message.vue'
import PencilIcon from './icons/Pencil.vue'
import ContactEditIcon from './icons/Contact.vue'
import PapersIcon from './icons/ContactsList.vue'
import ChatMessageIcon from './icons/Chat.vue'
import ScheduleIcon from './icons/Schedule.vue'
import PhoneIcon from './icons/PhoneList.vue'
import SiteIcon from './icons/Site.vue'
import SupportIcon from './icons/Support.vue'
import PackageIcon from './icons/Package.vue'
import UsersIcon from './icons/Users.vue'
import SmsIcon from './icons/SMS.vue'
import SettingsIcon from './icons/Settings.vue'

export default {
  name: 'SidenavItems',
  components: {
    CubesIcon,
    ChatIcon,
    ContactEditIcon,
    PencilIcon,
    PapersIcon,
    ChatMessageIcon,
    ScheduleIcon,
    PhoneIcon,
    SiteIcon,
    SupportIcon,
    PackageIcon,
    UsersIcon,
    SmsIcon,
    SettingsIcon,
    Accordion,
    SidenavItem
  },
  inject: ['state', 'toggle'],
}
</script>
