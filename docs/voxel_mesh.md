# VoxelMesh

## Functions

| Function Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| SetVoxel([Vector](vector) pos, [VoxelAsset](voxel_asset) voxel) | None | Change a single voxel in world space | Server Only |
| SetVoxelBox([Vector](vector) pos, [Vector](vector) dimensions, [VoxelAsset](voxel_asset) voxel) | None | Change a cuboid of voxels with given dimensions in world units (centimeters). 1 voxel = 25cm | Server Only |
| SetVoxelBox([Vector](vector) pos, number halfSize, [VoxelAsset](voxel_asset) voxel) | None | Change a cube of voxels with a given half-size in world units (centimeters) for each axis. 1 voxel = 25cm | Server Only |
| SetVoxelSphere([Vector](vector) pos, [Vector](vector) dimensions, [VoxelAsset](voxel_asset) voxel) | None | Change an elipsoid of voxels with given dimensions in world units (centimeters). 1 voxel = 25cm | Server Only |
| SetVoxelSphere([Vector](vector) pos, number radius, [VoxelAsset](voxel_asset) voxel) | None | Change a sphere of voxels with a given radius in world units (centimeters). 1 voxel = 25cm | Server |
| ResetVoxels() | None | Reset any SetVoxel...() calls that have been done during play, returning the voxel prop to its starting state (ie as it was in the editor) | Server Only |
| CreateThruster() | [Thruster](thruster) | Add a thruster to a voxel mesh	| None |
| CreateRelativeThruster() | [Thruster](thruster) | Add a thruster to a voxel mesh	| None |
| DestroyThruster([Thruster](thruster) handle) | None | Destroy a thruster	| None |
| AddImpulse([Vector](vector) impulse) | None | Add Impulse. An integral of force over a time interval. Newton seconds | None |
| AddAngularImpulse([Rotation](rotation) rotation) | None | Add an angular impulse. An integral of torque over a time interval. Newton seconds | None |

## Properties

| Property Name | Return Type | Description | Tags |
|---------------|-------------|-------------|------|
| mesh | [MeshAsset](mesh_asset) | Set or get the mesh asset | Read-Write |
| collisionEnabled | boolean | Turn on or off collision (ie calling entry point OnCollision) | Read-Write |
| damageEnabled | boolean | Turn on or off damage (ie calling of entry point OnDamaged) | Read-Write |
| physicsEnabled | boolean | Turn on or off physics | Read-Write |
| gravityEnabled | boolean | Turn on or off gravity | Read-Write |
| onCollision | Event | Called when this entity is collided with by a player Character with the Character passed as an argument, as well as the voxel mesh Entity from which the onCollision event was sent. An alternative to listening for OnCollision in a script on the entity | Read |
| onDamage | Event | Called when this entity is damaged with the amount of damage, the entity causing the damage and a HitResult structure, as well as the voxel mesh Entity from which the onDamage event was sent. An alternative to listening for OnDamage in a script on the entity | Read |

## Examples