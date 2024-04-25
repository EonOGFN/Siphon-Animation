# "Siphon" Animation
- The Animation itself is improper, it's not the correct animation but rather something very similar, depending on what you're trying to use it for.

      void AFortPlayerPawn::ApplySiphonAnimation()
      {
          static auto SlurpBarrelClass = FindObject<UClass>(L"/Game/Athena/Items/Gameplay/SilkyBingo/Athena_Prop_SilkyBingo.Athena_Prop_SilkyBingo_C"); // slurp barrel
      
          if (!SlurpBarrelClass)
              return;
      
          FVector Loc = GetActorLocation();
          Loc.Z += 500; // z = height, 500 = 5 meters 
      
          auto NewActor = GetWorld()->SpawnActor<AActor>(SlurpBarrelClass, Loc);
      
          if (NewActor)
              NewActor->K2_DestroyActor(); // destroys slurp barrel
      } 

---
**Note: I will not provide support for this code. Please refrain from DMing me regarding where to place it. Use a little bit of your brain, its very straightforward.**
**Credits:** I honestly have no clue who originally created the code, but it has spread to many places. Therefore, I decided to share it on GitHub.
