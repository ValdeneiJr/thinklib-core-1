# Changelog

## 0.1.3 — 2025-08-12

* **Fix:** erros de compilação (**CS1671**) corrigidos ao mover atributos (`AddComponentMenu`, `RequireComponent` etc.) **para dentro** dos `namespace` nos scripts:

  * `Runtime/Platformer/Core/ProjectileShooterBase.cs`
  * `Runtime/Platformer/Enemy/Types/Shooter/EnemyShooterAI.cs`
  * `Runtime/Topdown/Combat/ProjectileTopdownShooterBase.cs`
  * `Runtime/Topdown/Enemy/Types/Shooter/TopdownEnemyShooterAI.cs`
* **Fix:** ajustes nos **asmdefs**:

  * `com.thinklib.core` (Runtime) **não** referencia o assembly de Editor.
  * `com.thinklib.core.Editor` com `includePlatforms: ["Editor"]` e referência ao Runtime.
  * Resolve aviso/erro do Burst sobre `com.thinklib.core.Editor`.
* **Chore:** limpeza de `.meta` órfãos e pastas de **Editor** fora do lugar sob `Runtime/`.
* **Fix:** estabilidade de prefabs (remoção/ajuste de referências aninhadas ausentes).
* **UX:** componentes Thinklib aparecendo corretamente no menu **Component → Thinklib → …**.

## 0.1.2 — 2025-08-12 *(deprecated)*

* **IMPORTANTE:** versão descontinuada por conter erros de namespace que impediam a compilação em alguns projetos.
* **Novo:** menu **Component → Thinklib → …** para adicionar componentes rapidamente.
* Adicionados `AddComponentMenu` nos scripts principais para aparecerem no menu *Component*.
* **Editor:** ajustes de UX nos *inspectors* (rótulos padronizados, seções agrupadas, avisos).
* **Chore:** limpeza de *namespaces* e referências de asmdefs.

## 0.1.1 — 2025-08-11

* **Release funcional; 0.1.0 marcado como *deprecated*.**
* Corrigida instalação via UPM (Git URL) com `package.json` válido e metadados.
* Scripts de Editor realocados para `Editor/` (root) garantindo separação de compilação.
* Geradores de assets/prefabs agora salvam em `Assets/Thinklib/...` (evita erro de pasta imutável em `Packages/`).
* **Inspectors personalizados:**

  * Platformer: `EnemyShooterAI`
  * Topdown: `TopdownEnemyShooterAI`
* Estabilidade nos criadores de Animator Controllers e na auto-criação de pastas.

## 0.1.0 — 2025-08-10 *(deprecated)*

* Initial public release
* Package structure (Runtime/Editor) with asmdefs
* Animator Controller creators:

  * Platformer: Player & Enemy
  * Topdown: Player & Enemy (2D Blend Trees)
* Point & Click menu items: Item and Combination Recipe (ScriptableObjects)
* Auto-creation of asset folders under `Assets/Thinklib/...`
* Dependencies via UPM: TextMesh Pro, UGUI
