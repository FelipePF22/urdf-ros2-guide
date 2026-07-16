# Manual de Instrução para Construção de Modelos URDF
> Guia Prático de Modelagem e Estruturação no ROS 2

Este repositório contém as diretrizes técnicas, boas práticas e exemplos práticos para o desenvolvimento, parametrização e validação de arquivos **URDF (Unified Robot Description Format)**. O conteúdo é baseado no manual de instruções desenvolvido na **Escola de Engenharia de São Carlos da Universidade de São Paulo (EESC-USP)**.

**O Mesmo contem também sua versão em inglês (It also includes an English version.)**

---

## 📌 Conteúdo do Guia

O repositório e o manual estão estruturados para cobrir todo o pipeline de desenvolvimento, desde a preparação dos ativos 3D até a simulação em ambientes modernos:

1. **Preparação das Partes e Malhas Tridimensionais (Blender)**
   * Organização estrutural e importação de arquivos CAD para o Blender (versão recomendada: `4.5.5 LTS`).
   * Correção de escalas (conversão de milímetros para metros).
   * Alinhamento exato do centro geométrico e pontos de articulação (origens/pivôs) para juntas móveis e fixas.
   * Otimização, junção de peças estáticas (`Join`) e exportação para arquivos COLLADA (`.dae`) e STL customizados.
2. **Criação da Pasta e Configuração do Ambiente ROS 2**
   * Estruturação padronizada da árvore de diretórios do pacote ROS 2 (`ament_python`).
   * Gerenciamento de dependências através do `package.xml`.
   * Mapeamento dinâmico de recursos (malhas, launchs, rviz) através do `setup.py`.
   * Integração com o Gazebo utilizando o manifesto `model.config`.
3. **Anatomia e Codificação do URDF**
   * Definição e detalhamento de blocos essenciais: `<visual>`, `<collision>` e `<inertial>`.
   * Modelagem de matrizes de inércia e centros de massa.
   * Guia prático dos 6 tipos primitivos de juntas: `fixed`, `continuous`, `revolute`, `prismatic`, `planar` e `floating`.
4. **Automatização e Injeção Física (Launch Files)**
   * Utilização do `robot_state_publisher` e `joint_state_publisher_gui`.
   * Scripts de inicialização em Python (`display.launch.py`) com sincronização de tempo (`use_sim_time`).
   * Injeção limpa de robôs em tempo de execução via `spawn_entity.py`.
5. **Compatibilidade com NVIDIA Isaac Sim**
   * Como converter arquivos e macros parametrizadas do Xacro para URDFs estáticos e resolvidos.
---


## 📌 Conteúdo adicional 

O repositório contem um regra de ouro na montagem de URDFs, com o titulo: `"Regra_de_montagem_URDF"`

---

## 📄 Licença e Referência

Este trabalho e os exemplos contidos neste repositório foram desenvolvidos com base no referencial teórico e prático de:

* **Autor:** Felipe Pereira Furlaneto
* **Contato:** ffurlaneto@usp.br
* **Instituição:** Escola de Engenharia de São Carlos - Universidade de São Paulo (EESC-USP)

O código e as especificações deste repositório estão licenciados sob a **Licença Apache 2.0**. Sinta-se livre para utilizar e distribuir, desde que seja mantido os devidos créditos e referências ao autor original e à instituição.

```text
Copyright 2026 Felipe Pereira Furlaneto (EESC-USP)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
