1) What are Channels and Kernels (according to EVA)? 
Channels:
     * An Image can be divided into number of colours called channels.
     * For Ex: Suppose an image is constituted of 3 colours R, G and B.
       Then, it can be divided into 3 channels each representing one colour.
     * Ex 2: Consider a multi-coloured beaded ornament having 4 different colours(Red, Blue, yellow, orange) of beads.
       Multiple bead channels are formed when specific colour of beads are extracted along with their exact location.
       Hence, Each channel becomes a layer of the ornament having all information about Red/blue/yellow/orange colour beads.
       Once, all the channels are superimposed, results in the original bead ornament with exact colour bead placed in original location.
       
Kernel:
    Kernel has different names such as filter, matrix, feature extractor etc.,
    Ex: if each bead channels constitute beads of same colour, then, kernels are those filters which extract the beads based on colour.
    
 2) Why should we only (well mostly) use 3x3 Kernels?
      * 3x3 kernels are extensively used due to the following reasons:
            - Contains Line of symmetry through which computations can be done on left side (x-1,y) and right side (x+1,y) if centre pixel               is (x,y).
            - Local receptive field of 1 pixel (3x3 kernel) = 3x3 pixels (original image). 
              So, each pixel in the kernel shall have information from 9 pixels which are closely placed with one another.
              Hence, more relevant information can be extracted rather than using 5x5 / 7x7 kernels where information from farther pixels                 are also extracted and may not be relevant.
            - Simple, less expensive and efficient 
            - 3x3 kernel shall result in more channels as compared to 5x5 / 7x7 which may help to extract more information on similar                     features.
            
  3) How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 ? (show calculations)
       * To achieve Global Receptive feed of 199x199 we need to add nearly 98 layers.
         199x199 | 3x3 > 197x197
         197x197 | 3x3 > 195x195
         195x195 | 3x3 > 193x193
         193x193 | 3x3 > 191x191
         191x191 | 3x3 > 189x189
         189x189 | 3x3 > 187x187
         187x187 | 3x3 > 185x185
         185x185 | 3x3 > 183x183
         183x183 | 3x3 > 181x181
         181x181 | 3x3 > 179x179
         179x179 | 3x3 > 177x177
         177x177 | 3x3 > 175x175
         175x175 | 3x3 > 173x173
         173x173 | 3x3 > 171x171
         171x171 | 3x3 > 169x169
         169x169 | 3x3 > 167x167
         167x167 | 3x3 > 165x165
         165x165 | 3x3 > 163x163
         163x163 | 3x3 > 161x161
         161x161 | 3x3 > 159x159
         159x159 | 3x3 > 157x157
         157x157 | 3x3 > 155x155
         155x155 | 3x3 > 153x153
         153x153 | 3x3 > 151x151
         151x151 | 3x3 > 149x149
         149x149 | 3x3 > 147x147
         147x147 | 3x3 > 145x145
         145x145 | 3x3 > 143x143
         143x143 | 3x3 > 141x141
         141x141 | 3x3 > 139x139
         139x139 | 3x3 > 137x137
         137x137 | 3x3 > 135x135
         135x135 | 3x3 > 133x133
         133x133 | 3x3 > 131x131
         131x131 | 3x3 > 129x129
         129x129 | 3x3 > 127x127
         127x127 | 3x3 > 125x125
         125x125 | 3x3 > 123x123
         123x123 | 3x3 > 121x121
         121x121 | 3x3 > 119x119
         119x119 | 3x3 > 117x117
         117x117 | 3x3 > 115x115
         115x115 | 3x3 > 113x113
         113x113 | 3x3 > 111x111
         111x111 | 3x3 > 109x109
         109x109 | 3x3 > 107x107
         107x107 | 3x3 > 105x105
         105x105 | 3x3 > 103x103
         103x103 | 3x3 > 101x101
         101x101 | 3x3 > 99 x 99
         99 x 99 | 3x3 > 97 x 97
         97 x 97 | 3x3 > 95 x 95
         95 x 95 | 3x3 > 93 x 93
         93 x 93 | 3x3 > 91 x 91
         91 x 91 | 3x3 > 89 x 89
         89 x 89 | 3x3 > 87 x 87
         87 x 87 | 3x3 > 85 x 85
         85 x 85 | 3x3 > 83 x 83
         83 x 83 | 3x3 > 81 x 81
         81 x 81 | 3x3 > 79 x 79
         79 x 79 | 3x3 > 77 x 77
         77 x 77 | 3x3 > 75 x 75
         75 x 75 | 3x3 > 73 x 73
         73 x 73 | 3x3 > 71 x 71
         71 x 71 | 3x3 > 69 x 69
         69 x 69 | 3x3 > 67 x 67
         67 x 67 | 3x3 > 65 x 65
         65 x 65 | 3x3 > 63 x 63
         63 x 63 | 3x3 > 61 x 61
         61 x 61 | 3x3 > 59 x 59
         59 x 59 | 3x3 > 57 x 57
         57 x 57 | 3x3 > 55 x 55
         55 x 55 | 3x3 > 53 x 53
         53 x 53 | 3x3 > 51 x 51
         51 x 51 | 3x3 > 49 x 49
         49 x 49 | 3x3 > 47 x 47
         47 x 47 | 3x3 > 45 x 45
         45 x 45 | 3x3 > 43 x 43
         43 x 43 | 3x3 > 41 x 41
         41 x 41 | 3x3 > 39 x 39
         39 x 39 | 3x3 > 37 x 37
         37 x 37 | 3x3 > 35 x 35
         35 x 35 | 3x3 > 33 x 33
         33 x 33 | 3x3 > 31 x 31
         31 x 31 | 3x3 > 29 x 29
         29 x 29 | 3x3 > 27 x 27
         27 x 27 | 3x3 > 25 x 25
         25 x 25 | 3x3 > 23 x 23
         23 x 23 | 3x3 > 21 x 21
         21 x 21 | 3x3 > 19 x 19
         19 x 19 | 3x3 > 17 x 17
         17 x 17 | 3x3 > 15 x 15
         15 x 15 | 3x3 > 13 x 13
         13 x 13 | 3x3 > 11 x 11
         11 x 11 | 3x3 > 09 x 09
         09 x 09 | 3x3 > 07 x 07
         07 x 07 | 3x3 > 05 x 05
         05 x 05 | 3x3 > 03 x 03
         03 x 03 | 3x3 > 01 x 01         
         
         
         
      
       
