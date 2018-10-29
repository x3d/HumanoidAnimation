# 4.9.6 Hierarchy
* http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy

---

## LOA-0 hierarchy

LOA-0 includes only one *joint : segment* pair, as follows:

**[LOA-0]** humanoid_root : sacrum

---

## 4.9.6.1 LOA-1 hierarchy 
* http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy1

**[LOA-0]** humanoid_root : sacrum

  **[LOA-1]** sacroiliac : pelvis
  
  | **[LOA-1]** l_hip : l_thigh
  
  | | **[LOA-1]** l_knee : l_calf
  
```
  | |   l_talocrural : l_hindfoot
  | |     l_metatarsophalangeal : l_middistal
  | r_hip : r_thigh
  |   r_knee : r_calf
  |     r_talocrural : r_hindfoot
  |       r_metatarsophalangeal : r_middistal
  vl5 : l5
    skullbase : skull
    l_shoulder : l_upperarm
    | l_elbow : l_forearm
    |   l_radiocarpal : l_hand
    r_shoulder : r_upperarm
      r_elbow : r_forearm
        r_radiocarpal : r_hand
```

### Figure 4.10 — Basic set of Joint:Segment hierarchy for LOA-1 (joint name : segment name)

---

## 4.9.6.2 LOA-2 hierarchy
* http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy2

```
**[LOA-0]** humanoid_root : sacrum
  **[LOA-1]** sacroiliac : pelvis
  | **[LOA-1]** l_hip : l_thigh
  | | **[LOA-1]** l_knee : l_calf
  | |   l_talocrural : l_talus
  | |     l_tarsometatarsal : l_metatarsal
  | |       l_metatarsophalangeal : l_tarsal_proximal_phalanx
  | |         l_tarsal_interphalangeal : l_tarsal_distal_phalanx
  | r_hip : r_thigh
  |   r_knee : r_calf
  |     r_talocrural : r_talus
  |       r_tarsometatarsal : r_metatarsal
  |         r_metatarsophalangeal : r_tarsal_proximal_phalanx
  |           r_tarsal_interphalangeal : r_tarsal_distal_phalanx
  vl5 : l5
    vl3 : l3
      vl1 : l1
        vt10 : t10
          vt6 : t6
            vt1 : t1
              vc4 : c4
              |   vc2 : c2
              |     skullbase : skull
              l_sternoclavicular : l_clavicle
              | l_acromioclavicular : l_scapula
              |   l_shoulder : l_upperarm
              |     l_elbow : l_forearm
              |       l_radiocarpal : l_carpal
              |         l_carpometacarpal_1 : l_metacarpal_1
              |         | l_metacarpophalangeal_1 : l_carpal_proximal_phalanx_1
              |         |   l_carpal_interphalangeal_1 : l_carpal_distal_phalanx_1
              |         l_carpometacarpal_2 : l_metacarpal_2
              |         | l_metacarpophalangeal_2 : l_carpal_proximal_phalanx_2
              |         |   l_carpal_proximal_interphalangeal_2 : l_carpal_middle_phalanx_2
              |         |     l_carpal_distal_interphalangeal_2 : l_carpal_distal_phalanx_2
              |         l_carpometacarpal_3 : l_metacarpal_3
              |         | l_metacarpophalangeal_3 : l_carpal_proximal_phalanx_3
              |         |  l_carpal_proximal_interphalangeal_3 : l_carpal_middle_phalanx_3
              |         |     l_carpal_distal_interphalangeal_3 : l_carpal_distal_phalanx_3
              |         l_carpometacarpal_4 : l_metacarpal_4
              |         | l_metacarpophalangeal_4 : l_carpal_proximal_phalanx_4
              |         |   l_carpal_proximal_interphalangeal_4 : l_carpal_middle_phalanx_4
              |         |     l_carpal_distal_interphalangeal_4 : l_carpal_distal_phalanx_4
              |         l_carpometacarpal_5 : l_metacarpal_5
              |           l_metacarpophalangeal_5 : l_carpal_proximal_phalanx_5
              |             l_carpal_proximal_interphalangeal_5 : l_carpal_middle_phalanx_5
              |               l_carpal_distal_interphalangeal_5 : l_carpal_distal_phalanx_5
              r_sternoclavicular : r_clavicle
                r_acromioclavicular : r_scapula
                  r_shoulder : r_upperarm
                    r_elbow : r_forearm
                      r_radiocarpal : r_carpal
                        r_carpometacarpal_1 : r_metacarpal_1
                        | r_metacarpophalangeal_1 : r_carpal_proximal_phalanx_1
                        |   r_carpal_interphalangeal_1 : r_carpal_distal_phalanx_1
                        r_carpometacarpal_2 : r_metacarpal_2
                        | r_metacarpophalangeal_2 : r_carpal_proximal_phalanx_2
                        |   r_carpal_proximal_interphalangeal_2 : r_carpal_middle_phalanx_2
                        |     r_carpal_distal_interphalangeal_2 : r_carpal_distal_phalanx_2
                        r_carpometacarpal_3 : r_metacarpal_3
                        | r_metacarpophalangeal_3 : r_carpal_proximal_phalanx_3
                        |   r_carpal_proximal_interphalangeal_3 : r_carpal_middle_phalanx_3
                        |     r_carpal_distal_interphalangeal_3 : r_carpal_distal_phalanx_3
                        r_carpometacarpal_4 : r_metacarpal_4
                        | r_metacarpophalangeal_4 : r_carpal_proximal_phalanx_4
                        |   r_carpal_proximal_interphalangeal_4 : r_carpal_middle_phalanx_4
                        |     r_carpal_distal_interphalangeal_4 : r_carpal_distal_phalanx_4
                        r_carpometacarpal_5 : r_metacarpal_5
                          r_metacarpophalangeal_5 : r_carpal_proximal_phalanx_5
                            r_carpal_proximal_interphalangeal_5 : r_carpal_middle_phalanx_5
                              r_carpal_distal_interphalangeal_5 : r_carpal_distal_phalanx_5
```

### Figure 4.11 — Basic set of Joint:Segment hierarchy for LOA-2

---

## 4.9.6.3 LOA-3 hierarchy
* http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy3

The LOA-3 hierarchy forming the basic set of Joint objects is specified in Figure 4.12 with the segment names listed after the joints to which they are attached.

```
**[LOA-0]** humanoid_root : sacrum
  **[LOA-1]** sacroiliac : pelvis
  | **[LOA-1]** l_hip : l_thigh
  | | **[LOA-1]** l_knee : l_calf
  | |   l_talocrural : l_talus
  | |     l_tarsometatarsal : l_metatarsal
  | |       l_metatarsophalangeal : l_tarsal_proximal_phalanx
  | |         l_tarsal_interphalangeal : l_tarsal_distal_phalanx
  | r_hip : r_thigh
  |   r_knee : r_calf
  |     r_talocrural : r_talus
  |       r_tarsometatarsal : r_metatarsal
  |         r_metatarsophalangeal : r_tarsal_proximal_phalanx
  |           r_tarsal_interphangeal : r_tarsal_distal_phalanx
  vl5 : l5
    vl4 : l4
      vl3 : l3
        vl2 : l2
          vl1 : l1
            vt12 : t12
              vt11 : t11
                vt10 : t10
                  vt9 : t9
                    vt8 : t8
                      vt7 : t7
                        vt6 : t6
                          vt5 : t5
                            vt4 : t4
                              vt3 : t3
                                vt2 : t2
                                  vt1 : t1
                                    vc7 : c7
                                    | vc6 : c6
                                    |   vc5 : c5
                                    |     vc4 : c4
                                    |       vc3 : c3
                                    |         vc2 : c2
                                    |           vc1 : c1
                                    |             skullbase : skull
                                    |               l_eyelid_joint : l_eyelid
                                    |               r_eyelid_joint : r_eyelid
                                    |               l_eyeball_joint : l_eyeball
                                    |               r_eyeball_joint : r_eyeball
                                    |               l_eyebrow_joint : l_eyebrow
                                    |               r_eyebrow_joint : r_eyebrow
                                    |               temporomandibular : jaw
                                    l_sternoclavicular : l_clavicle
                                    | l_acromioclavicular : l_scapula
                                    |   l_shoulder : l_upperarm
                                    |     l_elbow : l_forearm
                                    |       l_radiocarpal : l_carpal
                                    |         l_carpometacarpal_1 : l_metacarpal_1
                                    |         | l_metacarpophalangeal_1 : l_carpal_proximal_phalanx_1
                                    |         |   l_carpal_interphalangeal_1 : l_carpal_distal_phalanx_1
                                    |         l_carpometacarpal_2 : l_metacarpal_2
                                    |         | l_metacarpophalangeal_2 : l_carpal_proximal_phalanx_2
                                    |         |   l_carpal_proximal_interphalangeal_2 : l_carpal_middle_phalanx_2
                                    |         |     l_carpal_distal_interphalangeal_2 : l_carpal_distal_phalanx_2
                                    |         l_carpometacarpal_3 : l_metacarpal_3
                                    |         | l_metacarpophalangeal_3 : l_carpal_proximal_phalanx_3
                                    |         |   l_carpal_proximal_interphalangeal_3 : l_carpal_middle_phalanx_3
                                    |         |     l_carpal_distal_interphalangeal_3 : l_carpal_distal_phalanx_3
                                    |         l_carpometacarpal_4 : l_metacarpal_4
                                    |         | l_metacarpophalangeal_4 : l_carpal_proximal_phalanx_4
                                    |         |   l_carpal_proximal_interphalangeal_4 : l_carpal_middle_phalanx_4
                                    |         |     l_carpal_distal_interphalangeal_4 : l_carpal_distal_phalanx_4
                                    |         l_carpometacarpal_5 : l_metacarpal_5
                                    |           l_metacarpophalangeal_5 : l_carpal_proximal_phalanx_5
                                    |             l_carpal_proximal_interphalangeal_5 : l_carpal_middle_phalanx_5
                                    |               l_carpal_distal_interphalangeal_5 : l_carpal_distal_phalanx_5
                                    r_sternoclavicular : r_clavicle
                                      r_acromioclavicular : r_scapula
                                        r_shoulder : r_upperarm
                                          r_elbow : r_forearm
                                            r_radiocarpal : r_carpal
                                              r_carpometacarpal_1 : r_metacarpal_1
                                              | r_metacarpophalangeal_1 : r_carpal_proximal_phalanx_1
                                              |   r_carpal_interphalangeal_1 : r_carpal_distal_phalanx_1
                                              r_carpometacarpal_2 : r_metacarpal_2
                                              | r_metacarpophalangeal_2 : r_carpal_proximal_phalanx_2
                                              |   r_carpal_proximal_interphalangeal_2 : r_carpal_middle_phalanx_2
                                              |     r_carpal_distal_interphalangeal_2 : r_carpal_distal_phalanx_2
                                              r_carpometacarpal_3 : r_metacarpal_3
                                              | r_metacarpophalangeal_3 : r_carpal_proximal_phalanx_3
                                              |   r_carpal_proximal_interphalangeal_3 : r_carpal_middle_phalanx_3
                                              |     r_carpal_distal_interphalangeal_3 : r_carpal_distal_phalanx_3
                                              r_carpometacarpal_4 : r_metacarpal_4
                                              | r_metacarpophalangeal_4 : r_carpal_proximal_phalanx_4
                                              |   r_carpal_proximal_interphalangeal_4 : r_carpal_middle_phalanx_4
                                              |     r_carpal_distal_interphalangeal_4 : r_carpal_distal_phalanx_4
                                              r_carpometacarpal_5 : r_metacarpal_5
                                                r_metacarpophalangeal_5 : r_carpal_proximal_phalanx_5
                                                  r_carpal_proximal_interphalangeal_5 : r_carpal_middle_phalanx_5
                                                    r_carpal_distal_interphalangeal_5 : r_carpal_distal_phalanx_5
```

### Figure 4.12 — Basic set of Joint:Segment hierarchy for LOA-3

---

## 4.9.6.4 LOA-4 hierarchy
* http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy4

```
**[LOA-0]** humanoid_root : sacrum
  **[LOA-1]** sacroiliac : pelvis
  | **[LOA-1]** l_hip : l_thigh
  | | **[LOA-1]** l_knee : l_calf
  | |   l_talocrural : l_talus(l_hindfoot)
  | |     l_talocalcaneonavicular : l_navicular
  | |     | l_cuneonavicular_1 : l_cuneiform_1
  | |     | | l_tarsometatarsal_1 : l_metatarsal_1
  | |     | |   l_metatarsophalangeal_1 : l_tarsal_proximal_phalanx_1
  | |     | |     l_tarsal_interphalangeal_1 : l_tarsal_distal_phalanx_1
  | |     | l_cuneonavicular_2 : l_cuneiform_2
  | |     | | l_tarsometatarsal_2 : l_metatarsal_2
  | |     | |   l_metatarsophalangeal_2 : l_tarsal_proximal_phalanx_2
  | |     | |     l_tarsal_proximal_interphalangeal_2 : l_tarsal_middle_phalanx_2
  | |     | |       l_tarsal_distal_interphalangeal_2 : l_tarsal_distal_phalanx_2
  | |     | l_cuneonavicular_3 : l_cuneiform_3
  | |     |   l_tarsometatarsal_3  : l_metatarsal_3
  | |     |     l_metatarsophalangeal_3 : l_tarsal_proximal_phalanx_3
  | |     |       l_tarsal_proximal_interphalangeal_3 : l_tarsal_middle_phalanx_3
  | |     |         l_tarsal_distal_interphalangeal_3 : l_tarsal_distal_phalanx_3
  | |     l_calcaneuscuboid : l_calcaneus
  | |       l_transversetarsal : l_cuboid
  | |         l_tarsometatarsal_4 : l_metatarsal_4
  | |         | l_metatarsophalangeal_4 : l_tarsal_proximal_phalanx_4
  | |         |   l_tarsal_proximal_interphalangeal_4 : l_tarsal_middle_phalanx_4
  | |         |     l_tarsal_distal_interphalangeal_4 : l_tarsal_distal_phalanx_4
  | |         l_tarsometatarsal_5 : l_metatarsal_5
  | |           l_metatarsophalangeal_5 : l_tarsal_proximal_phalanx_5
  | |             l_tarsal_proximal_interphalangeal_5 : l_tarsal_middle_phalanx_5
  | |               l_tarsal_distal_interphalangeal_5 : l_tarsal_distal_phalanx_5
  | r_hip : r_thigh
  |   r_knee : r_calf
  |     r_talocrural : r_talus(l_hindfoot)
  |       r_talocalcaneonavicular : r_navicular
  |       | r_cuneonavicular_1 : r_cuneiform_1
  |       | | r_tarsometatarsal_1 : r_metatarsal_1
  |       | |   r_metatarsophalangeal_1 : r_tarsal_proximal_phalanx_1
  |       | |     r_tarsal_interphalangeal_1 : r_tarsal_distal_phalanx_1
  |       | r_cuneonavicular_2 : r_cuneiform_2
  |       | | r_tarsometatarsal_2 : r_metatarsal_2
  |       | |   r_metatarsophalangeal_2 : r_tarsal_proximal_phalanx_2
  |       | |     r_tarsal_proximal_interphalangeal_2 : r_tarsal_middle_phalanx_2
  |       | |       r_tarsal_distal_interphalangeal_2 : r_tarsal_distal_phalanx_2
  |       | r_cuneonavicular_3 : r_cuneiform_3
  |       |   r_tarsometatarsal_3  : r_metatarsal_3
  |       |     r_metatarsophalangeal_3 : r_tarsal_proximal_phalanx_3
  |       |       r_tarsal_proximal_interphalangeal_3 : r_tarsal_middle_phalanx_3
  |       |         r_tarsal_distal_interphalangeal_3 : r_tarsal_distal_phalanx_3
  |       r_calcaneuscuboid : r_calcaneus
  |         r_transversetarsal : r_cuboid
  |           r_tarsometatarsal_4 : r_metatarsal_4
  |           | r_metatarsophalangeal_4 : r_tarsal_proximal_phalanx_4
  |           |   r_tarsal_proximal_interphalangeal_4 : r_tarsal_middle_phalanx_4
  |           |     r_tarsal_distal_interphalangeal_4 : r_tarsal_distal_phalanx_4
  |           r_tarsometatarsal_5 : r_metatarsal_5
  |             r_metatarsophalangeal_5 : r_tarsal_proximal_phalanx_5
  |               r_tarsal_proximal_interphalangeal_5 : r_tarsal_middle_phalanx_5
  |                 r_tarsal_distal_interphalangeal_5 : r_tarsal_distal_phalanx_5
  vl5 : l5
   vl4 : l4
     vl3 : l3
       vl2 : l2
         vl1 : l1
           vt12 : t12
             vt11 : t11
               vt10 : t10
                 vt9 : t9
                   vt8 : t8
                     vt7 : t7
                       vt6 : t6
                         vt5 : t5
                           vt4 : t4
                             vt3 : t3
                               vt2 : t2
                                 vt1 : t1
                                   vc7 : c7
                                   |  vc6 : c6
                                   |   vc5 : c5
                                   |     vc4 : c4
                                   |       vc3 : c3
                                   |         vc2 : c2
                                   |           vc1 : c1
                                   |             skullbase : skull
                                   |               l_eyelid_joint : l_eyelid
                                   |               r_eyelid_joint : r_eyelid
                                   |               l_eyeball_joint : l_eyeball
                                   |               r_eyeball_joint : r_eyeball
                                   |               l_eyebrow_joint : l_eyebrow
                                   |               r_eyebrow_joint : r_eyebrow
                                   |               temporomandibular : jaw
                                   l_sternoclavicular : l_clavicle
                                   | l_acromioclavicular : l_scapula
                                   |   l_shoulder : l_upperarm
                                   |     l_elbow : l_forearm
                                   |       l_radiocarpal : l_carpal (l_hand)
                                   |         l_midcarpal_1 : l_trapezium
                                   |         | l_carpometacarpal_1 : l_metacarpal_1
                                   |         |   l_metacarpophalangeal_1 : l_carpal_proximal_phalanx_1
                                   |         |     l_carpal_interphalangeal_1 : l_carpal_distal_phalanx_1
                                   |         l_midcarpal_2 : l_trapezoid
                                   |         | l_carpometacarpal_2 : l_metacarpal_2
                                   |         |   l_metacarpophalangeal_2 : l_carpal_proximal_phalanx_2 
                                   |         |     l_carpal_proximal_interphalangeal_2 : l_carpal_middle_phalanx_2
                                   |         |       l_carpal_distal_interphalangeal_2 : l_carpal_distal_phalanx_2
                                   |         l_midcarpal_3 : l_capitate
                                   |         | l_carpometacarpal_3 : l_metacarpal_3
                                   |         |   l_metacarpophalangeal_3 : l_carpal_proximal_phalanx_3
                                   |         |     l_carpal_proximal_interphalangeal_3 : l_carpal_middle_phalanx_3
                                   |         |       l_carpal_distal_interphalangeal_3 : l_carpal_distal_phalanx_3
                                   |         l_midcarpal_4_5 : l_hamate
                                   |           l_carpometacarpal_4 : l_metacarpal_4
                                   |           | l_metacarpophalangeal_4 : l_carpal_proximal_phalanx_4
                                   |           |   l_carpal_proximal_interphalangeal_4 : l_carpal_middle_phalanx_4
                                   |           |     l_carpal_distal_interphalangeal_4 : l_carpal_distal_phalanx_4
                                   |           l_carpometacarpal_5 : l_metacarpal_5
                                   |             l_metacarpophalangeal_5 : l_carpal_proximal_phalanx_5
                                   |               l_carpal_proximal_interphalangeal_5 : l_carpal_middle_phalanx_5
                                   |                 l_carpal_distal_interphalangeal_5 : l_carpal_distal_phalanx_5
                                   r_sternoclavicular : r_clavicle
                                     r_acromioclavicular : r_scapula
                                       r_shoulder : r_upperarm
                                         r_elbow : r_forearm
                                           r_radiocarpal : r_carpal (r_hand)
                                             r_midcarpal_1 : r_trapezium
                                             | r_carpometacarpal_1 : r_metacarpal_1
                                             |   r_metacarpophalangeal_1 : r_carpal_proximal_phalanx_1
                                             |     r_carpal_interphalangeal_1 : r_carpal_distal_phalanx_1
                                             r_midcarpal_2 : l_trapezoid
                                             | r_carpometacarpal_2 : r_metacarpal_2
                                             |   r_metacarpophalangeal_2 : r_carpal_proximal_phalanx_2 
                                             |     r_carpal_proximal_interphalangeal_2 : r_carpal_middle_phalanx_2
                                             |       r_carpal_distal_interphalangeal_2 : r_carpal_distal_phalanx_2
                                             r_midcarpal_3 : r_capitate
                                             | r_carpometacarpal_3 : r_metacarpal_3
                                             |   r_metacarpophalangeal_3 : r_carpal_proximal_phalanx_3
                                             |     r_carpal_proximal_interphalangeal_3 : r_carpal_middle_phalanx_3
                                             |       r_carpal_distal_interphalangeal_3 : r_carpal_distal_phalanx_3
                                             r_midcarpal_4_5 : r_hamate
                                               r_carpometacarpal_4 : r_metacarpal_4
                                               | r_metacarpophalangeal_4 : r_carpal_proximal_phalanx_4
                                               |   r_carpal_proximal_interphalangeal_4 : r_carpal_middle_phalanx_4
                                               |     r_carpal_distal_interphalangeal_4 : r_carpal_distal_phalanx_4
                                               r_carpometacarpal_5 : r_metacarpal_5
                                                 r_metacarpophalangeal_5 : r_carpal_proximal_phalanx_5
                                                   r_carpal_proximal_interphalangeal_5 : r_carpal_middle_phalanx_5
                                                     r_carpal_distal_interphalangeal_5 : r_carpal_distal_phalanx_5
```

### Figure 4.13 — Basic set of Joint:Segment hierarchy for LOA-4

---
