# Learning IDP: Azure Compute

This repository focuses on mastering Azure compute services using Python and Azure SDK to build, manage, and automate compute infrastructure for Internal Development Platform (IDP) development.

## 🎯 Learning Objectives

By working through this repository, you will:

1. Master Azure Virtual Machine management with Python SDK
1. Understand Azure Container Instances (ACI) operations
1. Work with Azure Kubernetes Service (AKS) programmatically
1. Implement VM Scale Sets for auto-scaling
1. Manage Azure Batch for large-scale computing
1. Optimize compute resources for cost and performance
1. Implement security best practices for compute workloads

## 📚 Prerequisites

- Python 3.11 or higher
- Azure subscription with contributor access
- Azure CLI installed and configured
- Completed [learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk)
- Basic understanding of virtualization and containers
- Git and GitHub account

## 🗂️ Directory Structure

```
learning-idp-azure-compute/
├── README.md                          # This file
├── REFERENCES.md                      # Links to resources and related repos
├── pyproject.toml                     # Python project configuration
├── requirements.txt                   # Python dependencies
├── requirements-dev.txt               # Development dependencies
├── .python-version                    # Python version for pyenv
├── .gitignore                         # Git ignore patterns
├── .env.example                       # Environment variables template
│
├── docs/
│   ├── concepts/
│   │   ├── 01-compute-overview.md
│   │   ├── 02-vm-architecture.md
│   │   ├── 03-container-services.md
│   │   ├── 04-kubernetes-basics.md
│   │   ├── 05-scaling-strategies.md
│   │   └── 06-security-hardening.md
│   ├── guides/
│   │   ├── getting-started.md
│   │   ├── vm-management.md
│   │   ├── container-deployment.md
│   │   ├── aks-operations.md
│   │   └── cost-optimization.md
│   └── examples/
│       ├── simple-vm-deployment.md
│       ├── container-instance.md
│       ├── aks-cluster-setup.md
│       ├── vm-scale-set.md
│       └── batch-computing.md
│
├── src/
│   ├── __init__.py
│   │
│   ├── core/
│   │   ├── __init__.py
│   │   ├── authentication.py          # Azure authentication
│   │   ├── config.py                  # Configuration management
│   │   ├── exceptions.py              # Custom exceptions
│   │   └── logging_config.py          # Logging setup
│   │
│   ├── virtual_machines/
│   │   ├── __init__.py
│   │   ├── vm_manager.py              # VM CRUD operations
│   │   ├── vm_extensions.py           # VM extensions management
│   │   ├── vm_images.py               # Image management
│   │   └── vm_sizes.py                # VM size utilities
│   │
│   ├── disks/
│   │   ├── __init__.py
│   │   ├── disk_manager.py            # Disk operations
│   │   ├── snapshot_manager.py        # Snapshot management
│   │   └── disk_encryption.py         # Encryption operations
│   │
│   ├── availability/
│   │   ├── __init__.py
│   │   ├── availability_sets.py       # Availability sets
│   │   ├── availability_zones.py      # Availability zones
│   │   └── proximity_groups.py        # Proximity placement groups
│   │
│   ├── scale_sets/
│   │   ├── __init__.py
│   │   ├── vmss_manager.py            # VMSS operations
│   │   ├── autoscale.py               # Auto-scaling configuration
│   │   └── load_balancer.py           # Load balancer integration
│   │
│   ├── containers/
│   │   ├── __init__.py
│   │   ├── aci_manager.py             # Container Instances
│   │   ├── container_groups.py        # Container groups
│   │   └── registry.py                # Container Registry operations
│   │
│   ├── kubernetes/
│   │   ├── __init__.py
│   │   ├── aks_manager.py             # AKS cluster management
│   │   ├── node_pools.py              # Node pool operations
│   │   ├── addons.py                  # AKS addons
│   │   └── kubernetes_client.py       # Kubernetes API client
│   │
│   ├── batch/
│   │   ├── __init__.py
│   │   ├── batch_accounts.py          # Batch account management
│   │   ├── pools.py                   # Batch pool operations
│   │   └── jobs.py                    # Batch job management
│   │
│   └── monitoring/
│       ├── __init__.py
│       ├── diagnostics.py             # Diagnostic settings
│       ├── metrics.py                 # Performance metrics
│       └── health_checks.py           # Health monitoring
│
├── examples/
│   ├── 01_virtual_machines/
│   │   ├── 01_create_simple_vm.py
│   │   ├── 02_create_vm_with_data_disk.py
│   │   ├── 03_vm_operations.py
│   │   ├── 04_vm_extensions.py
│   │   └── 05_vm_custom_script.py
│   │
│   ├── 02_managed_disks/
│   │   ├── 01_create_managed_disk.py
│   │   ├── 02_attach_disk_to_vm.py
│   │   ├── 03_disk_snapshots.py
│   │   └── 04_disk_encryption.py
│   │
│   ├── 03_availability/
│   │   ├── 01_availability_set.py
│   │   ├── 02_availability_zones.py
│   │   └── 03_proximity_placement.py
│   │
│   ├── 04_scale_sets/
│   │   ├── 01_create_vmss.py
│   │   ├── 02_autoscale_rules.py
│   │   ├── 03_rolling_upgrades.py
│   │   └── 04_load_balancer_integration.py
│   │
│   ├── 05_containers/
│   │   ├── 01_simple_container.py
│   │   ├── 02_container_group.py
│   │   ├── 03_multi_container_group.py
│   │   ├── 04_container_registry.py
│   │   └── 05_aci_networking.py
│   │
│   ├── 06_kubernetes/
│   │   ├── 01_create_aks_cluster.py
│   │   ├── 02_manage_node_pools.py
│   │   ├── 03_aks_networking.py
│   │   ├── 04_aks_addons.py
│   │   ├── 05_deploy_application.py
│   │   └── 06_aks_monitoring.py
│   │
│   ├── 07_batch/
│   │   ├── 01_create_batch_account.py
│   │   ├── 02_create_batch_pool.py
│   │   ├── 03_submit_batch_job.py
│   │   └── 04_monitor_batch_job.py
│   │
│   └── 08_advanced/
│       ├── 01_spot_instances.py
│       ├── 02_gpu_workloads.py
│       ├── 03_hybrid_connectivity.py
│       ├── 04_disaster_recovery.py
│       └── 05_cost_optimization.py
│
├── templates/
│   ├── vm/
│   │   ├── linux_vm.json              # Linux VM ARM template
│   │   ├── windows_vm.json            # Windows VM ARM template
│   │   └── custom_image.json          # Custom image template
│   ├── vmss/
│   │   ├── vmss_basic.json            # Basic VMSS template
│   │   └── vmss_autoscale.json        # VMSS with autoscale
│   ├── aks/
│   │   ├── aks_basic.json             # Basic AKS template
│   │   └── aks_advanced.json          # Advanced AKS configuration
│   └── scripts/
│       ├── cloud_init.yml             # Cloud-init configuration
│       ├── install_docker.sh          # Docker installation
│       └── configure_monitoring.sh    # Monitoring setup
│
├── notebooks/
│   ├── 01_vm_basics.ipynb
│   ├── 02_container_services.ipynb
│   ├── 03_kubernetes_operations.ipynb
│   ├── 04_scaling_strategies.ipynb
│   └── 05_cost_analysis.ipynb
│
├── scripts/
│   ├── setup_compute_environment.sh   # Setup script
│   ├── cleanup_resources.sh           # Cleanup script
│   └── cost_report.py                 # Cost reporting
│
├── tests/
│   ├── __init__.py
│   ├── conftest.py
│   ├── unit/
│   │   ├── test_vm_manager.py
│   │   ├── test_disk_manager.py
│   │   ├── test_aci_manager.py
│   │   └── test_aks_manager.py
│   └── integration/
│       ├── test_vm_lifecycle.py
│       ├── test_vmss_operations.py
│       ├── test_aci_deployment.py
│       └── test_aks_cluster.py
│
└── .github/
    └── workflows/
        ├── test.yml                   # Run tests
        ├── examples.yml               # Test examples
        └── cleanup.yml                # Cleanup resources
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/vanHeemstraSystems/learning-idp-azure-compute.git
cd learning-idp-azure-compute
```

### 2. Set Up Python Environment

```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment
# On Linux/MacOS:
source venv/bin/activate
# On Windows:
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
pip install -r requirements-dev.txt
```

### 3. Configure Azure Authentication

```bash
# Login to Azure
az login

# Set subscription
az account set --subscription "your-subscription-id"

# Create service principal (optional, for automation)
az ad sp create-for-rbac --name "idp-compute-sp" --role Contributor

# Configure environment variables
cp .env.example .env
# Edit .env with your credentials
```

### 4. Run Your First Example

```bash
# Create a simple Linux VM
python examples/01_virtual_machines/01_create_simple_vm.py

# List all VMs
python examples/01_virtual_machines/03_vm_operations.py --action list

# Create a container instance
python examples/05_containers/01_simple_container.py
```

## 📖 Learning Path

Follow this recommended sequence:

### Week 1: Virtual Machines Fundamentals

**Day 1-2: Understanding Azure VMs**

1. Read `docs/concepts/01-compute-overview.md`
1. Study `docs/concepts/02-vm-architecture.md`
1. Run `examples/01_virtual_machines/01_create_simple_vm.py`

**Day 3-4: VM Management**

1. Read `docs/guides/vm-management.md`
1. Work through all examples in `examples/01_virtual_machines/`
1. Practice VM operations: start, stop, restart, delete

**Day 5-7: Disks and Storage**

1. Complete examples in `examples/02_managed_disks/`
1. Practice disk attachment and detachment
1. Implement disk snapshots and backups

### Week 2: High Availability & Scaling

**Day 1-2: Availability Patterns**

1. Study `docs/concepts/05-scaling-strategies.md`
1. Complete examples in `examples/03_availability/`
1. Implement availability sets and zones

**Day 3-5: VM Scale Sets**

1. Work through `examples/04_scale_sets/`
1. Configure auto-scaling rules
1. Implement rolling upgrades

**Day 6-7: Load Balancing**

1. Configure load balancers
1. Implement health probes
1. Practice traffic distribution

### Week 3: Containers & Kubernetes

**Day 1-2: Container Instances**

1. Read `docs/concepts/03-container-services.md`
1. Complete examples in `examples/05_containers/`
1. Deploy multi-container groups

**Day 3-5: Azure Kubernetes Service**

1. Study `docs/concepts/04-kubernetes-basics.md`
1. Work through `examples/06_kubernetes/`
1. Deploy applications to AKS

**Day 6-7: Advanced AKS**

1. Configure networking and security
1. Implement monitoring and logging
1. Practice cluster scaling

### Week 4: Advanced Topics

**Day 1-2: Batch Computing**

1. Complete examples in `examples/07_batch/`
1. Implement batch job processing
1. Monitor batch operations

**Day 3-5: Optimization & Security**

1. Study `docs/concepts/06-security-hardening.md`
1. Work through `examples/08_advanced/`
1. Implement cost optimization strategies

**Day 6-7: Production Readiness**

1. Disaster recovery planning
1. Monitoring and alerting setup
1. Complete end-to-end scenarios

## 🔑 Key Azure SDK Packages

### Compute Management

```python
# Virtual Machines
azure-mgmt-compute>=30.0.0          # VMs, disks, images, VMSS

# Container Services
azure-mgmt-containerinstance>=10.1.0 # Container Instances
azure-mgmt-containerservice>=28.0.0  # AKS
azure-mgmt-containerregistry>=10.1.0 # Container Registry

# Batch Computing
azure-mgmt-batch>=17.0.0            # Batch accounts and operations

# Supporting Services
azure-mgmt-network>=25.0.0          # Networking for compute
azure-mgmt-storage>=21.0.0          # Storage for compute
azure-mgmt-monitor>=6.0.0           # Monitoring
```

## 💡 Common Operations Examples

### Create a Linux Virtual Machine

```python
from azure.identity import DefaultAzureCredential
from azure.mgmt.compute import ComputeManagementClient
from azure.mgmt.network import NetworkManagementClient

credential = DefaultAzureCredential()
compute_client = ComputeManagementClient(credential, subscription_id)
network_client = NetworkManagementClient(credential, subscription_id)

# Create network interface
nic_params = {
    'location': 'westeurope',
    'ip_configurations': [{
        'name': 'ipconfig1',
        'subnet': {'id': subnet_id},
        'public_ip_address': {'id': public_ip_id}
    }]
}
nic = network_client.network_interfaces.begin_create_or_update(
    'my-rg',
    'my-vm-nic',
    nic_params
).result()

# Create virtual machine
vm_params = {
    'location': 'westeurope',
    'hardware_profile': {
        'vm_size': 'Standard_B2s'
    },
    'storage_profile': {
        'image_reference': {
            'publisher': 'Canonical',
            'offer': 'UbuntuServer',
            'sku': '18.04-LTS',
            'version': 'latest'
        },
        'os_disk': {
            'name': 'my-vm-os-disk',
            'caching': 'ReadWrite',
            'create_option': 'FromImage',
            'managed_disk': {
                'storage_account_type': 'Standard_LRS'
            }
        }
    },
    'os_profile': {
        'computer_name': 'myvm',
        'admin_username': 'azureuser',
        'admin_password': 'P@ssw0rd1234!',  # Use SSH keys in production
        'linux_configuration': {
            'disable_password_authentication': False
        }
    },
    'network_profile': {
        'network_interfaces': [{
            'id': nic.id,
            'primary': True
        }]
    }
}

vm_creation = compute_client.virtual_machines.begin_create_or_update(
    'my-rg',
    'my-vm',
    vm_params
)
vm = vm_creation.result()
print(f"Created VM: {vm.name}")
```

### Create Container Instance

```python
from azure.identity import DefaultAzureCredential
from azure.mgmt.containerinstance import ContainerInstanceManagementClient
from azure.mgmt.containerinstance.models import (
    ContainerGroup,
    Container,
    ContainerPort,
    Port,
    IpAddress,
    ResourceRequirements,
    ResourceRequests,
    OperatingSystemTypes
)

credential = DefaultAzureCredential()
aci_client = ContainerInstanceManagementClient(credential, subscription_id)

# Define container
container = Container(
    name='mycontainer',
    image='mcr.microsoft.com/azuredocs/aci-helloworld',
    resources=ResourceRequirements(
        requests=ResourceRequests(memory_in_gb=1.5, cpu=1.0)
    ),
    ports=[ContainerPort(port=80)]
)

# Define container group
container_group = ContainerGroup(
    location='westeurope',
    containers=[container],
    os_type=OperatingSystemTypes.linux,
    ip_address=IpAddress(
        ports=[Port(protocol='TCP', port=80)],
        type='Public'
    )
)

# Create container group
aci_creation = aci_client.container_groups.begin_create_or_update(
    'my-rg',
    'my-container-group',
    container_group
)
container_group = aci_creation.result()
print(f"Container IP: {container_group.ip_address.ip}")
```

### Create AKS Cluster

```python
from azure.identity import DefaultAzureCredential
from azure.mgmt.containerservice import ContainerServiceClient
from azure.mgmt.containerservice.models import (
    ManagedCluster,
    ManagedClusterAgentPoolProfile,
    ContainerServiceLinuxProfile,
    ContainerServiceSshConfiguration,
    ContainerServiceSshPublicKey
)

credential = DefaultAzureCredential()
aks_client = ContainerServiceClient(credential, subscription_id)

# Define agent pool
agent_pool = ManagedClusterAgentPoolProfile(
    name='nodepool1',
    count=3,
    vm_size='Standard_DS2_v2',
    mode='System'
)

# Define Linux profile
ssh_config = ContainerServiceSshConfiguration(
    public_keys=[
        ContainerServiceSshPublicKey(key_data='your-ssh-public-key')
    ]
)
linux_profile = ContainerServiceLinuxProfile(
    admin_username='azureuser',
    ssh=ssh_config
)

# Create AKS cluster
aks_params = ManagedCluster(
    location='westeurope',
    dns_prefix='myaks',
    agent_pool_profiles=[agent_pool],
    linux_profile=linux_profile,
    identity={
        'type': 'SystemAssigned'
    }
)

aks_creation = aks_client.managed_clusters.begin_create_or_update(
    'my-rg',
    'my-aks-cluster',
    aks_params
)
aks_cluster = aks_creation.result()
print(f"Created AKS cluster: {aks_cluster.name}")
```

### Create VM Scale Set with Auto-scaling

```python
from azure.identity import DefaultAzureCredential
from azure.mgmt.compute import ComputeManagementClient
from azure.mgmt.monitor import MonitorManagementClient

credential = DefaultAzureCredential()
compute_client = ComputeManagementClient(credential, subscription_id)
monitor_client = MonitorManagementClient(credential, subscription_id)

# Create VMSS
vmss_params = {
    'location': 'westeurope',
    'sku': {
        'name': 'Standard_B2s',
        'tier': 'Standard',
        'capacity': 2
    },
    'upgrade_policy': {
        'mode': 'Automatic'
    },
    'virtual_machine_profile': {
        'storage_profile': {
            'image_reference': {
                'publisher': 'Canonical',
                'offer': 'UbuntuServer',
                'sku': '18.04-LTS',
                'version': 'latest'
            }
        },
        'os_profile': {
            'computer_name_prefix': 'vmss',
            'admin_username': 'azureuser',
            'admin_password': 'P@ssw0rd1234!'
        },
        'network_profile': {
            'network_interface_configurations': [{
                'name': 'vmss-nic',
                'primary': True,
                'ip_configurations': [{
                    'name': 'ipconfig1',
                    'subnet': {'id': subnet_id},
                    'load_balancer_backend_address_pools': [
                        {'id': backend_pool_id}
                    ]
                }]
            }]
        }
    }
}

vmss = compute_client.virtual_machine_scale_sets.begin_create_or_update(
    'my-rg',
    'my-vmss',
    vmss_params
).result()

# Configure auto-scale
autoscale_settings = {
    'location': 'westeurope',
    'profiles': [{
        'name': 'Auto scale based on CPU',
        'capacity': {
            'minimum': '2',
            'maximum': '10',
            'default': '2'
        },
        'rules': [{
            'metric_trigger': {
                'metric_name': 'Percentage CPU',
                'metric_resource_id': vmss.id,
                'time_grain': 'PT1M',
                'statistic': 'Average',
                'time_window': 'PT5M',
                'time_aggregation': 'Average',
                'operator': 'GreaterThan',
                'threshold': 75
            },
            'scale_action': {
                'direction': 'Increase',
                'type': 'ChangeCount',
                'value': '1',
                'cooldown': 'PT5M'
            }
        }, {
            'metric_trigger': {
                'metric_name': 'Percentage CPU',
                'metric_resource_id': vmss.id,
                'time_grain': 'PT1M',
                'statistic': 'Average',
                'time_window': 'PT5M',
                'time_aggregation': 'Average',
                'operator': 'LessThan',
                'threshold': 25
            },
            'scale_action': {
                'direction': 'Decrease',
                'type': 'ChangeCount',
                'value': '1',
                'cooldown': 'PT5M'
            }
        }]
    }],
    'enabled': True,
    'target_resource_id': vmss.id
}

autoscale = monitor_client.autoscale_settings.create_or_update(
    'my-rg',
    'vmss-autoscale',
    autoscale_settings
)
print(f"Configured auto-scaling for: {vmss.name}")
```

## 🎯 Best Practices

### 1. VM Management

```python
# Use managed identities instead of credentials
from azure.identity import ManagedIdentityCredential

credential = ManagedIdentityCredential()

# Always use managed disks
'os_disk': {
    'create_option': 'FromImage',
    'managed_disk': {
        'storage_account_type': 'Premium_LRS'  # SSD for better performance
    }
}

# Enable boot diagnostics
'diagnostics_profile': {
    'boot_diagnostics': {
        'enabled': True,
        'storage_uri': storage_account_uri
    }
}
```

### 2. Security Hardening

```python
# Disable password authentication, use SSH keys
'linux_configuration': {
    'disable_password_authentication': True,
    'ssh': {
        'public_keys': [{
            'path': '/home/azureuser/.ssh/authorized_keys',
            'key_data': ssh_public_key
        }]
    }
}

# Enable disk encryption
from azure.mgmt.compute.models import DiskEncryptionSettings

disk_encryption = DiskEncryptionSettings(
    enabled=True,
    disk_encryption_key={
        'secret_url': key_vault_secret_url,
        'source_vault': {'id': key_vault_id}
    }
)
```

### 3. Cost Optimization

```python
# Use spot instances for non-critical workloads
'priority': 'Spot',
'eviction_policy': 'Deallocate',
'billing_profile': {
    'max_price': -1  # Pay up to on-demand price
}

# Use burstable VM sizes for variable workloads
'vm_size': 'Standard_B2s'  # B-series for cost savings

# Auto-shutdown for dev/test VMs
# Configure through Azure Portal or use scheduled actions
```

### 4. Monitoring and Diagnostics

```python
# Enable VM diagnostics
from azure.mgmt.compute.models import DiagnosticsProfile

diagnostics = DiagnosticsProfile(
    boot_diagnostics={
        'enabled': True,
        'storage_uri': diagnostic_storage_uri
    }
)

# Configure VM insights
# Install Azure Monitor agent as VM extension
```

## 🔧 Development Tools

### Essential Tools

```bash
# Install Azure CLI
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash

# Install kubectl for AKS
az aks install-cli

# Install Docker for container development
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

# Code quality tools
black src/ examples/
ruff check src/ examples/
mypy src/
```

### Testing

```bash
# Run unit tests
pytest tests/unit/

# Run integration tests (creates real Azure resources)
pytest tests/integration/ --azure-subscription-id your-sub-id

# Run with coverage
pytest --cov=src --cov-report=html
```

## 📊 Performance Benchmarking

### VM Performance Testing

```python
# Example: Benchmark disk I/O
import time
from azure.mgmt.compute import ComputeManagementClient

def benchmark_disk_io(vm_name, resource_group):
    """Run disk I/O benchmark on VM"""
    compute_client = ComputeManagementClient(credential, subscription_id)
    
    # Run command on VM
    command = {
        'command_id': 'RunShellScript',
        'script': [
            'dd if=/dev/zero of=/tmp/test bs=1M count=1024',
            'sync',
            'echo "Write test complete"',
            'dd if=/tmp/test of=/dev/null bs=1M',
            'echo "Read test complete"'
        ]
    }
    
    result = compute_client.virtual_machines.begin_run_command(
        resource_group,
        vm_name,
        command
    ).result()
    
    return result.value[0].message
```

## 🔗 Related Repositories

- [learning-internal-development-platform](https://github.com/vanHeemstraSystems/learning-internal-development-platform) - Main overview
- [learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk) - Azure SDK fundamentals
- [learning-idp-azure-networking](https://github.com/vanHeemstraSystems/learning-idp-azure-networking) - Network configuration
- [learning-idp-azure-storage](https://github.com/vanHeemstraSystems/learning-idp-azure-storage) - Storage management
- [learning-idp-infrastructure-as-code](https://github.com/vanHeemstraSystems/learning-idp-infrastructure-as-code) - IaC patterns

## 🤝 Contributing

This is a personal learning repository, but suggestions and improvements are welcome!

1. Fork the repository
1. Create a feature branch
1. Make your changes with tests
1. Ensure all tests pass
1. Submit a pull request

## 📄 License

This project is for educational purposes. See LICENSE file for details.

## 📧 Contact

Willem van Heemstra

- GitHub: [@vanHeemstraSystems](https://github.com/vanHeemstraSystems)
- LinkedIn: [Willem van Heemstra](https://www.linkedin.com/in/willemvanheemstra/)

-----

*Last updated: December 18, 2025*
*Part of the learning-internal-development-platform series*
