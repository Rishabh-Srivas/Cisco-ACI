Create Access Port Playbook :
- name: Create Application Profile
  cisco.aci.aci_ap:
    hostname: "{{ apic_hostname }}"
    username: "{{ apic_username }}"
    password: "{{ apic_password }}"
    tenant: "{{ apic_tenant }}"
    ap: "{{ apic_app_proile }}"
    description: Intranet Portal
    monitoring_policy: default
    state: present
    validate_certs: false


  Create Bridge Domain Playbook :

    - name: Add a Bridge Domain
    cisco.aci.aci_bd:
      hostname: "{{ apic_hostname }}"
      username: "{{ apic_username }}"
      password: "{{ apic_password }}"
      tenant: "{{ apic_tenant }}"
      vrf: "{{ apic_vrf }}"
      bd: "{{ apic_bd }}"
      state: present
      validate_certs: false




      
