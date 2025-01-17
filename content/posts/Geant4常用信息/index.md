+++
date = '2022-02-22'
draft = false
title = 'Geant4常用信息'
tags = ['Science', 'Code', 'Simulation']
+++

获取一些粒子蒙卡输运step中的常用信息
```
G4StepPoint*  preStepPoint = step->GetPreStepPoint();//step的前端点
G4StepPoint* postStepPoint = step->GetPostStepPoint();//step的后端点
G4String particleID = step->GetTrack()->GetParticleDefinition()->GetParticleName();//获取粒子名称
//printf("%s\n", particleID.c_str());//在终端实时打印粒子名称

if (preStepPoint->GetStepStatus() == fGeomBoundary){
G4double xStep = step->GetPreStepPoint()->GetPosition().x();//x坐标
G4double yStep = step->GetPreStepPoint()->GetPosition().y();//y坐标
G4double zStep = step->GetPreStepPoint()->GetPosition().z();//z坐标
    G4double energy = step->GetTrack()->GetDynamicParticle()->GetKineticEnergy();//粒子动能
}
```

```
step‐>GetPreStepPoint()‐>GetGlobalTime();  
// get current track information  
G4Track* track = step‐>GetTrack();
/* some examples of track information */  
track‐>GetParticleDefinition() 
// ‐> Get Particle informations  
track‐>GetTrackID();  
track‐>GetParentID();  
track‐>GetCurrentStepNumber();  
track‐>GetKineticEnergy();
```

```
G4int eventID = (G4EventManager::GetEventManager())->GetConstCurrentEvent()->GetEventID();
// 因为在step里面，我使用EventManager这个类去获取EventID
G4int trackID = step->GetTrack()->GetTrackID();

G4String particleName =  step->GetTrack()->GetDefinition()->GetParticleName();

G4String postProcessName = step->GetPostStepPoint()->GetProcessDefinedStep()->GetProcessName();

G4String preName = step->GetPreStepPoint()->GetTouchableHandle()->GetVolume()->GetName();

G4double postKE = step->GetPostStepPoint()->GetKineticEnergy();
G4double preKE = step->GetPreStepPoint()->GetKineticEnergy();

G4double edepStep = step->GetTotalEnergyDeposit();
```

```
G4String creatorName;
if (trackID==1)  creatorName="primary";
else creatorName = step->GetTrack()->GetCreatorProcess()->GetProcessName();
```

```
G4String postName;
if (step->GetPostStepPoint()->GetStepStatus() == fWorldBoundary) postName="out";
else postName = step->GetPostStepPoint()->GetTouchableHandle()->GetVolume()->GetName();
```
