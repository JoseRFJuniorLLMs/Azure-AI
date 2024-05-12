• Face detection is the action of locating human faces in an image and optionally returning different kinds of face-related data. 
• Attributes 
• Accessories. Whether the given face has accessories. This attribute returns possible accessories including headwear, glasses, and mask, with confidence score between zero and one for each accessory.
• Age. The estimated age in years of a particular face.
• Blur. The blurriness of the face in the image. This attribute returns a value between zero and one and an informal rating of low, medium, or high. 
• Emotion. A list of emotions with their detection confidence for the given face. Confidence scores are normalized, and the scores across all emotions add up to one. The emotions returned are happiness, sadness, neutral, anger, contempt, disgust, surprise, and fear. 
• Exposure. The exposure of the face in the image. This attribute returns a value between zero and one and an informal rating of underExposure, goodExposure, or overExposure. 
• Facial hair. The estimated facial hair presence and the length for the given face.
• Gender. The estimated gender of the given face. Possible values are male, female, and genderless. 
• Glasses. Whether the given face has eyeglasses. Possible values are NoGlasses, ReadingGlasses, Sunglasses, and Swimming Goggles. 
• Hair. The hair type of the face. This attribute shows whether the hair is visible, whether baldness is detected, and what hair colors are detected. 
• Head pose. The face's orientation in 3D space. This attribute is described by the pitch, roll, and yaw angles in degrees. The value ranges are -90 degrees to 90 degrees, -90 degrees to 90 degrees, and -90 degrees to 90 degrees, respectively. See the following diagram for angle mappings: 
• Makeup. Whether the face has makeup. This attribute returns a Boolean value for eyeMakeup and lipMakeup. 
• Mask. Whether the face is wearing a mask. This attribute returns a possible mask type, and a Boolean value to indicate whether nose and mouth are covered. 
• Noise. The visual noise detected in the face image. This attribute returns a value between zero and one and an informal rating of low, medium, or high. 
• Occlusion. Whether there are objects blocking parts of the face. This attribute returns a Boolean value for eyeOccluded, foreheadOccluded, and mouthOccluded.
• Smile. The smile expression of the given face. This value is between zero for no smile and one for a clear smile.