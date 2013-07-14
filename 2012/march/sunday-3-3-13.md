Commit where the problems starts:
https://github.com/documentcloud/backbone/commit/5350dc9deaef3bd73430dba0ec0a5f52aec18192

#                __                       __
#   ____   _____/  |___  _  _____________|  | __
#  /    \_/ __ \   __\ \/ \/ /  _ \_  __ \  |/ /
# |   |  \  ___/|  |  \     (  <_> )  | \/    <
# |___|  /\___  >__|   \/\_/ \____/|__|  |__|_ \
#      \/     \/                              \/

def return_network(request, network):
    if network:
        return network
    return None


def return_networks(request, networks):
    return [return_network(request, network) for network in networks]


@view_config(route_name='clusterapi_network',
             request_method='GET',
             decorator=(api_exception_decorator_factory),
             renderer='json',
             xhr=True)
def network(request):
    """
        Basic querying of the Network model.
    """
    pass


@view_config(route_name='clusterapi_networks',
             request_method='GET',
             decorator=(api_exception_decorator_factory),
             renderer='json',
             xhr=True)
def networks(request):
    """
        Basic querying of the Network model.
    """
    pass


@view_config(route_name='clusterapi_networks',
             request_method='POST',
             decorator=(api_exception_decorator_factory),
             renderer='json',
             xhr=True)
def create_network(request):
    """
        Creates a Network record.
    """
    pass


@view_config(route_name='clusterapi_network',
             request_method='PUT',
             decorator=(api_exception_decorator_factory),
             renderer='json',
             xhr=True)
def update_network(request):
    """
        Updates a Network record.
    """
    pass


@view_config(route_name='clusterapi_network',
             request_method='DELETE',
             decorator=(api_exception_decorator_factory),
             renderer='json',
             xhr=True)
def delete_network(request):
    """
        Deletes a Network record.
    """
    pass