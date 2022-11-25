# TcComposite
Twincat 3.1 Composite pattern project

This is an experimental composite pattern project based on Twincat 3.1.
I don't have much experience in traditional programming, so this approach may seem naive.

The main objectives of this program are:
  - For simplicity's sake any FB extending Object FB will also be called an object,
  - Objects are declared as any other variable(VAR END_VAR),
  - Objects are automatically (FB_init, FB_exit) added or removed to or from their parent object,
  - Each object has a unique, automatically generated name. This name is based on its path,
  - Children can be extracted from parents by their name,
  - Helper functions are used to modify the extracted objects,
  - Children can execute the parent 'Refresh' method.
  - There is a logger singleton that keeps all events in an array of strings,
  
  
 Known issues:
  - After the second 'New Download' or 'Online Change' runtime crashes. CPU usage rises to 70-80%, and General Protection Error occur.
    It doesn't seem like there is a problem with the code.
    
    
 Planned features:
  - Observer Pattern. Example: EL1008[4].Attach_Sub(GVL.Tank.Get_Child('lvl_low')); OR F_Attach_Sub(EL1008[4], GVL.Tank.Get_Child('lvl_low'));
  - Objects don't need to be called in every iteration, but some do. Create a dynamic object list that holds only currently executed objects, such as timers, etc.
  - Better logs
