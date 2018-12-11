# Comparison Tables for Level Of Articulation (LOA)

## 4.9.6 Hierarchy
* http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy

Review notes

* These tables are copied from the HAnim specification
* The specification does not call out LOA-0
* '''*MISMATCH*''' indicates inconsistent segment names

---

## LOA-0 hierarchy (annotated)

LOA-0 includes only one named *joint : segment* pair, as follows:

```
[LOA-#] jointName : segmentName : siteName

[LOA-0] humanoid_root : sacrum
```

---

## 4.9.6.1 LOA-1 hierarchy (annotated) 
* Reference: [4.9.6.1 LOA-1 hierarchy](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy1)
* Reference: [4.9.7 Sites and Segment relationships](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#SiteSegmentRelationships)

```
[LOA-#] jointName : segmentName : siteName(s)

[LOA-0] humanoid_root : sacrum
  [LOA-1] sacroiliac : pelvis
  | [LOA-1] l_hip : l_thigh
  | | [LOA-1] l_knee : l_calf
  | |   [LOA-1] l_talocrural : l_hindfoot                               *MISMATCH talus/hindfoot*
  | |     [LOA-1] l_metatarsophalangeal : l_middistal                   *MISMATCH middistal/tarsal_proximal_phalanx*
  | [LOA-1] r_hip : r_thigh
  |   [LOA-1] r_knee : r_calf
  |     [LOA-1] r_talocrural : r_hindfoot                               *MISMATCH talus/hindfoot*
  |       [LOA-1] r_metatarsophalangeal : r_middistal                   *MISMATCH middistal/tarsal_proximal_phalanx*
  [LOA-1] vl5 : l5
    [LOA-1] skullbase : skull : skull_tip
    [LOA-1] l_shoulder : l_upperarm
    | [LOA-1] l_elbow : l_forearm
    |   [LOA-1] l_radiocarpal : l_hand                                  *MISMATCH hand/carpal*
    [LOA-1] r_shoulder : r_upperarm
      [LOA-1] r_elbow : r_forearm
        [LOA-1] r_radiocarpal : r_hand                                  *MISMATCH hand/carpal*
```

### Figure 4.10 — Basic set of Joint:Segment hierarchy for LOA-1 (joint name : segment name)

---

## 4.9.6.2 LOA-2 hierarchy (annotated)
* Reference: [4.9.6.2 LOA-2 hierarchy](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy2)
* Reference: [4.9.7 Sites and Segment relationships](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#SiteSegmentRelationships)

```
[LOA-#] jointName : segmentName : siteName(s)

[LOA-0] humanoid_root : sacrum
  [LOA-1] sacroiliac : pelvis
  | [LOA-1] l_hip : l_thigh
  | | [LOA-1] l_knee : l_calf
  | |   [LOA-1] l_talocrural : l_talus                                 *MISMATCH talus/hindfoot*
  | |     [LOA-2] l_tarsometatarsal : l_metatarsal
  | |       [LOA-1] l_metatarsophalangeal : l_tarsal_proximal_phalanx  *MISMATCH middistal/tarsal_proximal_phalanx*
  | |         [LOA-2] l_tarsal_interphalangeal : l_tarsal_distal_phalanx
  | [LOA-1] r_hip : r_thigh
  |   [LOA-1] r_knee : r_calf
  |     [LOA-1] r_talocrural : r_talus                                 *MISMATCH talus/hindfoot*
  |       [LOA-2] r_tarsometatarsal : r_metatarsal
  |         [LOA-1] r_metatarsophalangeal : r_tarsal_proximal_phalanx  *MISMATCH middistal/tarsal_proximal_phalanx*
  |           [LOA-2] r_tarsal_interphalangeal : r_tarsal_distal_phalanx
  [LOA-1] vl5 : l5
    [LOA-2] vl3 : l3
      [LOA-2] vl1 : l1
        [LOA-2] vt10 : t10
          [LOA-2] vt6 : t6
            [LOA-2] vt1 : t1
              [LOA-2] vc4 : c4
              |   [LOA-2] vc2 : c2
              |     [LOA-1] skullbase : skull : skull_tip
              [LOA-2] l_sternoclavicular : l_clavicle
              | [LOA-2] l_acromioclavicular : l_scapula
              |   [LOA-1] l_shoulder : l_upperarm
              |     [LOA-1] l_elbow : l_forearm
              |       [LOA-1] l_radiocarpal : l_carpal                *MISMATCH hand/carpal*
              |         [LOA-2] l_carpometacarpal_1 : l_metacarpal_1
              |         | [LOA-2] l_metacarpophalangeal_1 : l_carpal_proximal_phalanx_1
              |         |   [LOA-2] l_carpal_interphalangeal_1 : l_carpal_distal_phalanx_1
              |         [LOA-2] l_carpometacarpal_2 : l_metacarpal_2
              |         | [LOA-2] l_metacarpophalangeal_2 : l_carpal_proximal_phalanx_2
              |         |   [LOA-2] l_carpal_proximal_interphalangeal_2 : l_carpal_middle_phalanx_2
              |         |     [LOA-2] l_carpal_distal_interphalangeal_2 : l_carpal_distal_phalanx_2
              |         [LOA-2] l_carpometacarpal_3 : l_metacarpal_3
              |         | [LOA-2] l_metacarpophalangeal_3 : l_carpal_proximal_phalanx_3
              |         |  [LOA-2] l_carpal_proximal_interphalangeal_3 : l_carpal_middle_phalanx_3
              |         |     [LOA-2] l_carpal_distal_interphalangeal_3 : l_carpal_distal_phalanx_3
              |         [LOA-2] l_carpometacarpal_4 : l_metacarpal_4
              |         | [LOA-2] l_metacarpophalangeal_4 : l_carpal_proximal_phalanx_4
              |         |   [LOA-2] l_carpal_proximal_interphalangeal_4 : l_carpal_middle_phalanx_4
              |         |     [LOA-2] l_carpal_distal_interphalangeal_4 : l_carpal_distal_phalanx_4
              |         [LOA-2] l_carpometacarpal_5 : l_metacarpal_5
              |           [LOA-2] l_metacarpophalangeal_5 : l_carpal_proximal_phalanx_5
              |             [LOA-2] l_carpal_proximal_interphalangeal_5 : l_carpal_middle_phalanx_5
              |               [LOA-2] l_carpal_distal_interphalangeal_5 : l_carpal_distal_phalanx_5
              [LOA-2] r_sternoclavicular : r_clavicle
                [LOA-2] r_acromioclavicular : r_scapula
                  [LOA-1] r_shoulder : r_upperarm
                    [LOA-1] r_elbow : r_forearm
                      [LOA-1] r_radiocarpal : r_carpal                               *MISMATCH hand/carpal*
                        [LOA-2] r_carpometacarpal_1 : r_metacarpal_1
                        | [LOA-2] r_metacarpophalangeal_1 : r_carpal_proximal_phalanx_1
                        |   [LOA-2] r_carpal_interphalangeal_1 : r_carpal_distal_phalanx_1
                        [LOA-2] r_carpometacarpal_2 : r_metacarpal_2
                        | [LOA-2] r_metacarpophalangeal_2 : r_carpal_proximal_phalanx_2
                        |   [LOA-2] r_carpal_proximal_interphalangeal_2 : r_carpal_middle_phalanx_2
                        |     [LOA-2] r_carpal_distal_interphalangeal_2 : r_carpal_distal_phalanx_2
                        [LOA-2] r_carpometacarpal_3 : r_metacarpal_3
                        | [LOA-2] r_metacarpophalangeal_3 : r_carpal_proximal_phalanx_3
                        |   [LOA-2] r_carpal_proximal_interphalangeal_3 : r_carpal_middle_phalanx_3
                        |     [LOA-2] r_carpal_distal_interphalangeal_3 : r_carpal_distal_phalanx_3
                        [LOA-2] r_carpometacarpal_4 : r_metacarpal_4
                        | [LOA-2] r_metacarpophalangeal_4 : r_carpal_proximal_phalanx_4
                        |   [LOA-2] r_carpal_proximal_interphalangeal_4 : r_carpal_middle_phalanx_4
                        |     [LOA-2] r_carpal_distal_interphalangeal_4 : r_carpal_distal_phalanx_4
                        [LOA-2] r_carpometacarpal_5 : r_metacarpal_5
                          [LOA-2] r_metacarpophalangeal_5 : r_carpal_proximal_phalanx_5
                            [LOA-2] r_carpal_proximal_interphalangeal_5 : r_carpal_middle_phalanx_5
                              [LOA-2] r_carpal_distal_interphalangeal_5 : r_carpal_distal_phalanx_5
```

### Figure 4.11 — Basic set of Joint:Segment hierarchy for LOA-2

---

## 4.9.6.3 LOA-3 hierarchy (annotated)
* Reference: [4.9.6.3 LOA-3 hierarchy](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy3)
* Reference: [4.9.7 Sites and Segment relationships](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#SiteSegmentRelationships)

The LOA-3 hierarchy forming the basic set of Joint objects is specified in Figure 4.12 with the segment names listed after the joints to which they are attached.

```
[LOA-#] jointName : segmentName : siteName(s)

[LOA-0] humanoid_root : sacrum
  [LOA-1] sacroiliac : pelvis
  | [LOA-1] l_hip : l_thigh
  | | [LOA-1] l_knee : l_calf
  | |   [LOA-1] l_talocrural : l_talus                                 *MISMATCH talus/hindfoot*
  | |     [LOA-2] l_tarsometatarsal : l_metatarsal
  | |       [LOA-1] l_metatarsophalangeal : l_tarsal_proximal_phalanx  *MISMATCH middistal/tarsal_proximal_phalanx*
  | |         [LOA-2] l_tarsal_interphalangeal : l_tarsal_distal_phalanx
  | [LOA-1] r_hip : r_thigh
  |   [LOA-1] r_knee : r_calf
  |     [LOA-1] r_talocrural : r_talus                                 *MISMATCH talus/hindfoot*
  |       [LOA-2] r_tarsometatarsal : r_metatarsal
  |         [LOA-1] r_metatarsophalangeal : r_tarsal_proximal_phalanx  *MISMATCH middistal/tarsal_proximal_phalanx*
  |           [LOA-2] r_tarsal_interphalangeal : r_tarsal_distal_phalanx  *TYPO mispelled*
  [LOA-1] vl5 : l5
    [LOA-3] vl4 : l4
      [LOA-2] vl3 : l3
        [LOA-3] vl2 : l2
          [LOA-2] vl1 : l1
            [LOA-3] vt12 : t12
              [LOA-3] vt11 : t11
                [LOA-2] vt10 : t10
                  [LOA-3] vt9 : t9
                    [LOA-3] vt8 : t8
                      [LOA-3] vt7 : t7
                        [LOA-2] vt6 : t6
                          [LOA-3] vt5 : t5
                            [LOA-3] vt4 : t4
                              [LOA-3] vt3 : t3
                                [LOA-3] vt2 : t2
                                  [LOA-2] vt1 : t1
                                    [LOA-3] vc7 : c7
                                    | [LOA-3] vc6 : c6
                                    |   [LOA-3] vc5 : c5
                                    |     [LOA-2] vc4 : c4
                                    |       [LOA-3] vc3 : c3
                                    |         [LOA-2] vc2 : c2
                                    |           [LOA-3] vc1 : c1
                                    |             [LOA-1] skullbase : skull : skull_tip
                                    |               [LOA-3] l_eyelid_joint : l_eyelid
                                    |               [LOA-3] r_eyelid_joint : r_eyelid
                                    |               [LOA-3] l_eyeball_joint : l_eyeball
                                    |               [LOA-3] r_eyeball_joint : r_eyeball
                                    |               [LOA-3] l_eyebrow_joint : l_eyebrow
                                    |               [LOA-3] r_eyebrow_joint : r_eyebrow
                                    |               [LOA-3] temporomandibular : jaw
                                    [LOA-2] l_sternoclavicular : l_clavicle
                                    | [LOA-2] l_acromioclavicular : l_scapula
                                    |   [LOA-1] l_shoulder : l_upperarm
                                    |     [LOA-1] l_elbow : l_forearm
                                    |       [LOA-1] l_radiocarpal : l_carpal      *MISMATCH hand/carpal*
                                    |         [LOA-2] l_carpometacarpal_1 : l_metacarpal_1
                                    |         | [LOA-2] l_metacarpophalangeal_1 : l_carpal_proximal_phalanx_1
                                    |         |   [LOA-2] l_carpal_interphalangeal_1 : l_carpal_distal_phalanx_1
                                    |         [LOA-2] l_carpometacarpal_2 : l_metacarpal_2
                                    |         | [LOA-2] l_metacarpophalangeal_2 : l_carpal_proximal_phalanx_2
                                    |         |   [LOA-2] l_carpal_proximal_interphalangeal_2 : l_carpal_middle_phalanx_2
                                    |         |     [LOA-2] l_carpal_distal_interphalangeal_2 : l_carpal_distal_phalanx_2
                                    |         [LOA-2] l_carpometacarpal_3 : l_metacarpal_3
                                    |         | [LOA-2] l_metacarpophalangeal_3 : l_carpal_proximal_phalanx_3
                                    |         |   [LOA-2] l_carpal_proximal_interphalangeal_3 : l_carpal_middle_phalanx_3
                                    |         |     [LOA-2] l_carpal_distal_interphalangeal_3 : l_carpal_distal_phalanx_3
                                    |         [LOA-2] l_carpometacarpal_4 : l_metacarpal_4
                                    |         | [LOA-2] l_metacarpophalangeal_4 : l_carpal_proximal_phalanx_4
                                    |         |   [LOA-2] l_carpal_proximal_interphalangeal_4 : l_carpal_middle_phalanx_4
                                    |         |     [LOA-2] l_carpal_distal_interphalangeal_4 : l_carpal_distal_phalanx_4
                                    |         [LOA-2] l_carpometacarpal_5 : l_metacarpal_5
                                    |           [LOA-2] l_metacarpophalangeal_5 : l_carpal_proximal_phalanx_5
                                    |             [LOA-2] l_carpal_proximal_interphalangeal_5 : l_carpal_middle_phalanx_5
                                    |               [LOA-2] l_carpal_distal_interphalangeal_5 : l_carpal_distal_phalanx_5
                                    [LOA-2] r_sternoclavicular : r_clavicle
                                      [LOA-2] r_acromioclavicular : r_scapula
                                        [LOA-1] r_shoulder : r_upperarm
                                          [LOA-1] r_elbow : r_forearm
                                            [LOA-1] r_radiocarpal : r_carpal                               *MISMATCH hand/carpal*
                                              [LOA-2] r_carpometacarpal_1 : r_metacarpal_1
                                              | [LOA-2] r_metacarpophalangeal_1 : r_carpal_proximal_phalanx_1
                                              |   [LOA-2] r_carpal_interphalangeal_1 : r_carpal_distal_phalanx_1
                                              [LOA-2] r_carpometacarpal_2 : r_metacarpal_2
                                              | [LOA-2] r_metacarpophalangeal_2 : r_carpal_proximal_phalanx_2
                                              |   [LOA-2] r_carpal_proximal_interphalangeal_2 : r_carpal_middle_phalanx_2
                                              |     [LOA-2] r_carpal_distal_interphalangeal_2 : r_carpal_distal_phalanx_2
                                              [LOA-2] r_carpometacarpal_3 : r_metacarpal_3
                                              | [LOA-2] r_metacarpophalangeal_3 : r_carpal_proximal_phalanx_3
                                              |   [LOA-2] r_carpal_proximal_interphalangeal_3 : r_carpal_middle_phalanx_3
                                              |     [LOA-2] r_carpal_distal_interphalangeal_3 : r_carpal_distal_phalanx_3
                                              [LOA-2] r_carpometacarpal_4 : r_metacarpal_4
                                              | [LOA-2] r_metacarpophalangeal_4 : r_carpal_proximal_phalanx_4
                                              |   [LOA-2] r_carpal_proximal_interphalangeal_4 : r_carpal_middle_phalanx_4
                                              |     [LOA-2] r_carpal_distal_interphalangeal_4 : r_carpal_distal_phalanx_4
                                              [LOA-2] r_carpometacarpal_5 : r_metacarpal_5
                                                [LOA-2] r_metacarpophalangeal_5 : r_carpal_proximal_phalanx_5
                                                  [LOA-2] r_carpal_proximal_interphalangeal_5 : r_carpal_middle_phalanx_5
                                                    [LOA-2] r_carpal_distal_interphalangeal_5 : r_carpal_distal_phalanx_5
```

### Figure 4.12 — Basic set of Joint:Segment hierarchy for LOA-3

---

## 4.9.6.4 LOA-4 hierarchy (annotated)
* Reference: [4.9.6.4 LOA-4 hierarchy](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#Hierarchy4)
* Reference: [4.9.7 Sites and Segment relationships](http://www.web3d.org/documents/specifications/19774-1/V2.0/HAnim/concepts.html#SiteSegmentRelationships)

```
[LOA-#] jointName : segmentName : siteName(s)

[LOA-0] humanoid_root : sacrum
  [LOA-1] sacroiliac : pelvis
  | [LOA-1] l_hip : l_thigh
  | | [LOA-1] l_knee : l_calf
  | |   [LOA-1] l_talocrural : l_talus(l_hindfoot) *MISMATCH talus/hindfoot*
  | |     [LOA-4] l_talocalcaneonavicular : l_navicular
  | |     | [LOA-4] l_cuneonavicular_1 : l_cuneiform_1
  | |     | | [LOA-2] l_tarsometatarsal_1 : l_metatarsal_1                       *MISMATCH r_tarsometatarsal (no _1)*
  | |     | |   [LOA-4] l_metatarsophalangeal_1 : l_tarsal_proximal_phalanx_1
  | |     | |     [LOA-2] l_tarsal_interphalangeal_1 : l_tarsal_distal_phalanx_1 *MISMATCH l_tarsal_interphalangeal (no _1)*
  | |     | [LOA-4] l_cuneonavicular_2 : l_cuneiform_2
  | |     | | [LOA-4] l_tarsometatarsal_2 : l_metatarsal_2
  | |     | |   [LOA-4] l_metatarsophalangeal_2 : l_tarsal_proximal_phalanx_2
  | |     | |     [LOA-4] l_tarsal_proximal_interphalangeal_2 : l_tarsal_middle_phalanx_2
  | |     | |       [LOA-4] l_tarsal_distal_interphalangeal_2 : l_tarsal_distal_phalanx_2
  | |     | [LOA-4] l_cuneonavicular_3 : l_cuneiform_3
  | |     |   [LOA-4] l_tarsometatarsal_3  : l_metatarsal_3
  | |     |     [LOA-4] l_metatarsophalangeal_3 : l_tarsal_proximal_phalanx_3
  | |     |       [LOA-4] l_tarsal_proximal_interphalangeal_3 : l_tarsal_middle_phalanx_3
  | |     |         [LOA-4] l_tarsal_distal_interphalangeal_3 : l_tarsal_distal_phalanx_3
  | |     [LOA-4] l_calcaneuscuboid : l_calcaneus
  | |       [LOA-4] l_transversetarsal : l_cuboid
  | |         [LOA-4] l_tarsometatarsal_4 : l_metatarsal_4
  | |         | [LOA-4] l_metatarsophalangeal_4 : l_tarsal_proximal_phalanx_4
  | |         |   [LOA-4] l_tarsal_proximal_interphalangeal_4 : l_tarsal_middle_phalanx_4
  | |         |     [LOA-4] l_tarsal_distal_interphalangeal_4 : l_tarsal_distal_phalanx_4
  | |         [LOA-4] l_tarsometatarsal_5 : l_metatarsal_5
  | |           [LOA-4] l_metatarsophalangeal_5 : l_tarsal_proximal_phalanx_5
  | |             [LOA-4] l_tarsal_proximal_interphalangeal_5 : l_tarsal_middle_phalanx_5
  | |               [LOA-4] l_tarsal_distal_interphalangeal_5 : l_tarsal_distal_phalanx_5
  | [LOA-1] r_hip : r_thigh
  |   [LOA-1] r_knee : r_calf
  |     [LOA-1] r_talocrural : r_talus(l_hindfoot) *MISMATCH talus/hindfoot*
  |       [LOA-4] r_talocalcaneonavicular : r_navicular
  |       | [LOA-4] r_cuneonavicular_1 : r_cuneiform_1
  |       | | [LOA-2] r_tarsometatarsal_1 : r_metatarsal_1                        *MISMATCH r_tarsometatarsal (no _1)*
  |       | |   [LOA-4] r_metatarsophalangeal_1 : r_tarsal_proximal_phalanx_1
  |       | |     [LOA-2] r_tarsal_interphalangeal_1 : r_tarsal_distal_phalanx_1  *MISMATCH r_tarsal_interphalangeal (not _1)*
  |       | [LOA-4] r_cuneonavicular_2 : r_cuneiform_2
  |       | | [LOA-4] r_tarsometatarsal_2 : r_metatarsal_2
  |       | |   [LOA-4] r_metatarsophalangeal_2 : r_tarsal_proximal_phalanx_2
  |       | |     [LOA-4] r_tarsal_proximal_interphalangeal_2 : r_tarsal_middle_phalanx_2
  |       | |       [LOA-4] r_tarsal_distal_interphalangeal_2 : r_tarsal_distal_phalanx_2
  |       | [LOA-4] r_cuneonavicular_3 : r_cuneiform_3
  |       |   [LOA-4] r_tarsometatarsal_3  : r_metatarsal_3
  |       |     [LOA-4] r_metatarsophalangeal_3 : r_tarsal_proximal_phalanx_3
  |       |       [LOA-4] r_tarsal_proximal_interphalangeal_3 : r_tarsal_middle_phalanx_3
  |       |         [LOA-4] r_tarsal_distal_interphalangeal_3 : r_tarsal_distal_phalanx_3
  |       [LOA-4] r_calcaneuscuboid : r_calcaneus
  |         [LOA-4] r_transversetarsal : r_cuboid
  |           [LOA-4] r_tarsometatarsal_4 : r_metatarsal_4
  |           | [LOA-4] r_metatarsophalangeal_4 : r_tarsal_proximal_phalanx_4
  |           |   [LOA-4] r_tarsal_proximal_interphalangeal_4 : r_tarsal_middle_phalanx_4
  |           |     [LOA-4] r_tarsal_distal_interphalangeal_4 : r_tarsal_distal_phalanx_4
  |           [LOA-4] r_tarsometatarsal_5 : r_metatarsal_5
  |             [LOA-4] r_metatarsophalangeal_5 : r_tarsal_proximal_phalanx_5
  |               [LOA-4] r_tarsal_proximal_interphalangeal_5 : r_tarsal_middle_phalanx_5
  |                 [LOA-4] r_tarsal_distal_interphalangeal_5 : r_tarsal_distal_phalanx_5
  [LOA-1] vl5 : l5
   [LOA-3] vl4 : l4
     [LOA-2] vl3 : l3
       [LOA-3] vl2 : l2
         [LOA-2] vl1 : l1
           [LOA-3] vt12 : t12
             [LOA-3] vt11 : t11
               [LOA-2] vt10 : t10
                 [LOA-3] vt9 : t9
                   [LOA-3] vt8 : t8
                     [LOA-3] vt7 : t7
                       [LOA-2] vt6 : t6
                         [LOA-3] vt5 : t5
                           [LOA-3] vt4 : t4
                             [LOA-3] vt3 : t3
                               [LOA-3] vt2 : t2
                                 [LOA-2] vt1 : t1
                                   [LOA-3] vc7 : c7
                                   |  [LOA-3] vc6 : c6
                                   |   [LOA-3] vc5 : c5
                                   |     [LOA-2] vc4 : c4
                                   |       [LOA-3] vc3 : c3
                                   |         [LOA-2] vc2 : c2
                                   |           [LOA-3] vc1 : c1
                                   |             [LOA-1] skullbase : skull : skull_tip
                                   |               [LOA-3] l_eyelid_joint : l_eyelid
                                   |               [LOA-3] r_eyelid_joint : r_eyelid
                                   |               [LOA-3] l_eyeball_joint : l_eyeball
                                   |               [LOA-3] r_eyeball_joint : r_eyeball
                                   |               [LOA-3] l_eyebrow_joint : l_eyebrow
                                   |               [LOA-3] r_eyebrow_joint : r_eyebrow
                                   |               [LOA-3] temporomandibular : jaw
                                   [LOA-2] l_sternoclavicular : l_clavicle
                                   | [LOA-2] l_acromioclavicular : l_scapula
                                   |   [LOA-1] l_shoulder : l_upperarm
                                   |     [LOA-1] l_elbow : l_forearm
                                   |       [LOA-1] l_radiocarpal : l_carpal (l_hand)    *MISMATCH hand/carpal*
                                   |         [LOA-4] l_midcarpal_1 : l_trapezium
                                   |         | [LOA-2] l_carpometacarpal_1 : l_metacarpal_1
                                   |         |   [LOA-2] l_metacarpophalangeal_1 : l_carpal_proximal_phalanx_1
                                   |         |     [LOA-2] l_carpal_interphalangeal_1 : l_carpal_distal_phalanx_1
                                   |         [LOA-4] l_midcarpal_2 : l_trapezoid
                                   |         | [LOA-2] l_carpometacarpal_2 : l_metacarpal_2
                                   |         |   [LOA-2] l_metacarpophalangeal_2 : l_carpal_proximal_phalanx_2 
                                   |         |     [LOA-2] l_carpal_proximal_interphalangeal_2 : l_carpal_middle_phalanx_2
                                   |         |       [LOA-2] l_carpal_distal_interphalangeal_2 : l_carpal_distal_phalanx_2
                                   |         [LOA-4] l_midcarpal_3 : l_capitate
                                   |         | [LOA-2] l_carpometacarpal_3 : l_metacarpal_3
                                   |         |   [LOA-2] l_metacarpophalangeal_3 : l_carpal_proximal_phalanx_3
                                   |         |     [LOA-2] l_carpal_proximal_interphalangeal_3 : l_carpal_middle_phalanx_3
                                   |         |       [LOA-2] l_carpal_distal_interphalangeal_3 : l_carpal_distal_phalanx_3
                                   |         [LOA-4] l_midcarpal_4_5 : l_hamate
                                   |           [LOA-2] l_carpometacarpal_4 : l_metacarpal_4
                                   |           | [LOA-2] l_metacarpophalangeal_4 : l_carpal_proximal_phalanx_4
                                   |           |   [LOA-2] l_carpal_proximal_interphalangeal_4 : l_carpal_middle_phalanx_4
                                   |           |     [LOA-2] l_carpal_distal_interphalangeal_4 : l_carpal_distal_phalanx_4
                                   |           [LOA-2] l_carpometacarpal_5 : l_metacarpal_5
                                   |             [LOA-2] l_metacarpophalangeal_5 : l_carpal_proximal_phalanx_5
                                   |               [LOA-2] l_carpal_proximal_interphalangeal_5 : l_carpal_middle_phalanx_5
                                   |                 [LOA-2] l_carpal_distal_interphalangeal_5 : l_carpal_distal_phalanx_5
                                   [LOA-2] r_sternoclavicular : r_clavicle
                                     [LOA-2] r_acromioclavicular : r_scapula
                                       [LOA-1] r_shoulder : r_upperarm
                                         [LOA-1] r_elbow : r_forearm
                                           [LOA-1] r_radiocarpal : r_carpal (r_hand)                               *MISMATCH hand/carpal*
                                             [LOA-4] r_midcarpal_1 : r_trapezium
                                             | [LOA-2] r_carpometacarpal_1 : r_metacarpal_1
                                             |   [LOA-2] r_metacarpophalangeal_1 : r_carpal_proximal_phalanx_1
                                             |     [LOA-2] r_carpal_interphalangeal_1 : r_carpal_distal_phalanx_1
                                             [LOA-4] r_midcarpal_2 : l_trapezoid
                                             | [LOA-2] r_carpometacarpal_2 : r_metacarpal_2
                                             |   [LOA-2] r_metacarpophalangeal_2 : r_carpal_proximal_phalanx_2 
                                             |     [LOA-2] r_carpal_proximal_interphalangeal_2 : r_carpal_middle_phalanx_2
                                             |       [LOA-2] r_carpal_distal_interphalangeal_2 : r_carpal_distal_phalanx_2
                                             [LOA-4] r_midcarpal_3 : r_capitate
                                             | [LOA-2] r_carpometacarpal_3 : r_metacarpal_3
                                             |   [LOA-2] r_metacarpophalangeal_3 : r_carpal_proximal_phalanx_3
                                             |     [LOA-2] r_carpal_proximal_interphalangeal_3 : r_carpal_middle_phalanx_3
                                             |       [LOA-2] r_carpal_distal_interphalangeal_3 : r_carpal_distal_phalanx_3
                                             [LOA-4] r_midcarpal_4_5 : r_hamate
                                               [LOA-2] r_carpometacarpal_4 : r_metacarpal_4
                                               | [LOA-2] r_metacarpophalangeal_4 : r_carpal_proximal_phalanx_4
                                               |   [LOA-2] r_carpal_proximal_interphalangeal_4 : r_carpal_middle_phalanx_4
                                               |     [LOA-2] r_carpal_distal_interphalangeal_4 : r_carpal_distal_phalanx_4
                                               [LOA-2] r_carpometacarpal_5 : r_metacarpal_5
                                                 [LOA-2] r_metacarpophalangeal_5 : r_carpal_proximal_phalanx_5
                                                   [LOA-2] r_carpal_proximal_interphalangeal_5 : r_carpal_middle_phalanx_5
                                                     [LOA-2] r_carpal_distal_interphalangeal_5 : r_carpal_distal_phalanx_5
```

### Figure 4.13 — Basic set of Joint:Segment hierarchy for LOA-4

---

