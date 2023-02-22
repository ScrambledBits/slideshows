---
weight: 50
---
{{% section %}}
## How to Use the Diagrams Python Tool

------
{{<  div "fragment" >}}
Install the package using your favorite package manager

{{< code lang="shell" line-numbers="true" >}}
# using pip (pip3)
pip install diagrams

# using pipenv
pipenv install diagrams

# using poetry
poetry add diagrams
{{< /code >}}
{{< /div >}}
{{<  div "fragment" >}}
Start writing your python code...

{{< code lang="python" line-numbers="true" >}}
# filename = diagrams.py
from diagrams import Diagram
from diagrams.aws.compute import EC2
from diagrams.aws.database import RDS
from diagrams.aws.network import ELB

with Diagram("Web Service", show=False):
    ELB("lb") >> EC2("web") >> RDS("userdb")
{{< /code >}}
{{< /div >}}

------

Run the script
{{< code lang="shell" line-numbers="true" >}}
python diagrams.py
{{< /code >}}
{{% /section %}}
