######################################
#
# Aide pour pour créer des mods
# commentaire pour chaque ligne
#
######################################


[core]
# Les éléments de base de l'unité

name: MonUnité
# nom de l'unité en jeu

class: CustomUnitMetadata
# Signifie que c'est une unité personnalisée, à ne pas modifier

price: 100
# Prix de l'unité

maxHp: 240
# Points de vie de l'unité

mass: 500
# Masse de l'unité. Les plus lourdes poussent les plus légères en cas de collision

softCollisionOnAll: 3
# Délai avant l'application de la force de collision

techLevel: 1
# Le code couleur du niveau technologique

buildSpeed: 
# Temps nécessaire à la construction de l'unité

availableInDemo: 
# false pour exclure l'unité de la version démo du jeu, true pour l'autoriser

radius: 5
# rayon réel de collision de l'unité

displayRadius: 7
# rayon visible autour de l'unité sélectionnée

fogOfWarSightRange: 20
# Distance à laquelle l'unité lève le brouillard

isBio: false 
# Si true, l'unité est biologique et éclate à la mort. Si false, l'unité est mécanique et explose à la destruction

builtFrom_1_name: usineTank
# De quel constructeur provient cette unité

builtFrom_1_pos:  1
# Quel position occupe l'unité dans le menu de construction de son ctonstructeur

builtFrom_2_name: superUsine
# Si plusieurs constructeurs produisent cette unité, continuez la liste

builtFrom_2_pos:  2
# Si plusieurs constructeurs produisent cette unité, continuez la liste



[graphics]
# Les éléments du graphisme de l'unité

total_frames: 2
# Combien d'images composent le .png associé. Le moteur découpe le .png automatiquement ensuite pour créer l'animation

image:        monTank.png
# Nom du fichier de l'unité, doit correspondre au nom dans le dossier. Indispensable.

image_wreak:  monEpave.png
# Nom du fichier de l'unité détruite, doit correspondre au nom dans le dossier.
# Si aucune épave (pas de fichier, ou unité qui disparait totalement à sa mort), NONE

image_turret: maTourelle.png
# Nom du fichier de la tourelle, doit correspondre au nom dans le dossier.
# Si aucune tourelle, ou tourelle invible, NONE

scaleImagesTo: 20
# Modifie l'échelle de l'unité, par défaut 20 (la grille par défaut fait 20x20 pixels)

scaleTurretImagesTo: 9
#

animation_moving_start: 0
# Première image de l'animation (la première image est notée 0)

animation_moving_end: 1
# Dernière image de l'animation (la dernière image est notée n-1)

animation_moving_speed: 3
# Vitesse à laquelle l'animation doit être jouée. Plus c'est élevé, plus c'est lent.

lock_body_rotation_with_main_turret: true
# Si la tourelle est fixe, true. Si la tourelle tourne indépendamment, false.

image_shadow: AUTO
# Ombre de l'image, à laisser généralement sur AUTO ou NONE si pas d'ombre souhaitée

shadowOffsetX:1
# Décalage de l'ombre sur l'axe horizontal

shadowOffsetY:1
# Décalage de l'ombre sur l'axe vertical



[attack]
# Les élements de l'attaque de l'unité

turretRotateWithBody: false

canAttack: true
canAttackFlyingUnits: true
canAttackLandUnits:   true
canAttackUnderwaterUnits: false

turretSize: 7
turretTurnSpeed: 4


maxAttackRange: 110
shootDelay: 50

isFixedFiring: false



[turret_1]
invisible: true
x: 0
y: 0
idleDir:0

projectile: 1
size: 6
turnSpeed: 2.4

shoot_sound:plasma_fire
shoot_sound_vol:0.05
shoot_flame:small
shoot_light:#FFccCCEE


[projectile_1]
directDamage: 17
life: 70
speed: 6
frame: 5


[movement]
movementType: LAND
moveSpeed: 1.0
moveAccelerationSpeed: 0.03
moveDecelerationSpeed: 0.06

maxTurnSpeed: 2.4
turnAcceleration: 0.2

moveSlidingMode :false
moveIgnoringBody:false





